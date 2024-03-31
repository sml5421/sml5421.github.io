> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [docs.github.com](https://docs.github.com/en/actions/creating-actions/metadata-syntax-for-github-actions#about-yaml-syntax-for-github-actions)

> You can create actions to perform tasks in your repository. Actions require a metadata file that uses......

您可以创建操作以在存储库中执行任务。操作需要使用 YAML 语法的元数据文件。

[关于 GitHub Actions 的 YAML 语法](#about-yaml-syntax-for-github-actions)
--------------------------------------------------------------------

所有操作都需要元数据文件。元数据文件名必须是 或 。元数据文件中的数据定义操作的输入、输出和运行配置。`action.yml``action.yaml`

操作元数据文件使用 YAML 语法。如果您不熟悉 YAML，可以阅读 “[在五分钟内学习 YAML](https://www.codeproject.com/Articles/1214409/Learn-YAML-in-five-minutes)”。

[`name`](#name)
---------------

**必填**操作的名称。GitHub 在 **“操作**” 选项卡中显示，以帮助直观地识别每个作业中的操作。`name`

**自选**操作作者的姓名。

[`description`](#description)
-----------------------------

**必填**操作的简短说明。

[`inputs`](#inputs)
-------------------

**自选**输入参数允许您指定操作在运行时预期使用的数据。GitHub 将输入参数存储为环境变量。在运行时，带有大写字母的输入 ID 将转换为小写字母。我们建议使用小写的输入 ID。

### [示例：指定输入](#example-specifying-inputs)

此示例配置两个输入：和 。输入不是必需的，默认值为 。 是必需的，并且没有默认值。`num-octocats``octocat-eye-color``num-octocats``1``octocat-eye-color`

**注意：**如果未为自动触发工作流运行的事件指定输入，则工作流不会自动返回错误。如果您在工作流文件中设置并用于手动运行工作流，则需要在 GitHub.com 上指定输入。有关详细信息，请参阅 “[触发工作流的事件](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows)”。`required: true``required: true``workflow_dispatch`

使用此操作的工作流文件可以使用关键字设置 的输入值。有关语法的详细信息，请参阅 “[GitHub Actions 的工作流语法](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idstepswith)”。`with``octocat-eye-color``with`

```
inputs:
  num-octocats:
    description: 'Number of Octocats'
    required: false
    default: '1'
  octocat-eye-color:
    description: 'Eye color of the Octocats'
    required: true
```

当您在工作流文件中指定输入或使用默认输入值时，GitHub 会为输入创建一个名为 的环境变量。创建的环境变量将输入名称转换为大写字母，并将空格替换为字符。`INPUT_<VARIABLE_NAME>``_`

如果操作是使用[复合](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action)写入的，则它不会自动获得 。如果未进行转换，您可以手动更改这些输入。`INPUT_<VARIABLE_NAME>`

若要访问 Docker 容器操作中的环境变量，必须使用操作元数据文件中的关键字传递输入。有关 Docker 容器操作的操作元数据文件的详细信息，请参阅 “[创建 Docker 容器操作](https://docs.github.com/en/actions/creating-actions/creating-a-docker-container-action#creating-an-action-metadata-file)”。`args`

For example, if a workflow defined the and inputs, the action code could read the values of the inputs using the and environment variables.`num-octocats``octocat-eye-color``INPUT_NUM-OCTOCATS``INPUT_OCTOCAT-EYE-COLOR`

### [`inputs.<input_id>`](#inputsinput_id)

**Required** A identifier to associate with the input. The value of is a map of the input's metadata. The must be a unique identifier within the object. The must start with a letter or and contain only alphanumeric characters, , or .`string``<input_id>``<input_id>``inputs``<input_id>``_``-``_`

### [`inputs.<input_id>.description`](#inputsinput_iddescription)

**Required** A description of the input parameter.`string`

### [`inputs.<input_id>.required`](#inputsinput_idrequired)

**Optional** A to indicate whether the action requires the input parameter. Set to when the parameter is required.`boolean``true`

### [`inputs.<input_id>.default`](#inputsinput_iddefault)

**Optional** A representing the default value. The default value is used when an input parameter isn't specified in a workflow file.`string`

### [`inputs.<input_id>.deprecationMessage`](#inputsinput_iddeprecationmessage)

**Optional** If the input parameter is used, this is logged as a warning message. You can use this warning to notify users that the input is deprecated and mention any alternatives.`string`

[`outputs` for Docker container and JavaScript actions](#outputs-for-docker-container-and-javascript-actions)
-------------------------------------------------------------------------------------------------------------

**Optional** Output parameters allow you to declare data that an action sets. Actions that run later in a workflow can use the output data set in previously run actions. For example, if you had an action that performed the addition of two inputs (x + y = z), the action could output the sum (z) for other actions to use as an input.

Outputs are Unicode strings, and can be a maximum of 1 MB. The total of all outputs in a workflow run can be a maximum of 50 MB.

If you don't declare an output in your action metadata file, you can still set outputs and use them in a workflow. For more information on setting outputs in an action, see"[Workflow commands for GitHub Actions](https://docs.github.com/en/actions/using-workflows/workflow-commands-for-github-actions#setting-an-output-parameter)."

### [Example: Declaring outputs for Docker container and JavaScript actions](#example-declaring-outputs-for-docker-container-and-javascript-actions)

```
outputs:
  sum: # id of the output
    description: 'The sum of the inputs'
```

### [`outputs.<output_id>`](#outputsoutput_id)

**Required** A identifier to associate with the output. The value of is a map of the output's metadata. The must be a unique identifier within the object. The must start with a letter or and contain only alphanumeric characters, , or .`string``<output_id>``<output_id>``outputs``<output_id>``_``-``_`

### [`outputs.<output_id>.description`](#outputsoutput_iddescription)

**必填**输出参数的说明。`string`

[`outputs`对于复合操作](#outputs-for-composite-actions)
-------------------------------------------------

**可选**使用与 和 相同的参数（请参阅 “[Docker 容器和 JavaScript 操作`的输出`](#outputs-for-docker-container-and-javascript-actions)”），但也包括令牌。`outputs``outputs.<output_id>``outputs.<output_id>.description``value`

输出为 Unicode 字符串，最大为 1 MB。工作流运行中所有输出的总和最大为 50 MB。

### [示例：声明复合操作的输出](#example-declaring-outputs-for-composite-actions)

```
outputs:
  random-number:
    description: "Random number"
    value: ${{ steps.random-number-generator.outputs.random-id }}
runs:
  using: "composite"
  steps:
    - id: random-number-generator
      run: echo "random-id=$(echo $RANDOM)" >> $GITHUB_OUTPUT
      shell: bash
```

### [`outputs.<output_id>.value`](#outputsoutput_idvalue)

**必填**输出参数将映射到的值。您可以将其设置为具有上下文的表达式或表达式。例如，您可以使用上下文将输出设置为步骤的输出值。`string``steps``value`

有关如何使用上下文语法的详细信息，请参阅 “[上下文](https://docs.github.com/en/actions/learn-github-actions/contexts)”。

[`runs`](#runs)
---------------

**必填**指定这是 JavaScript 操作、复合操作还是 Docker 容器操作，以及该操作的执行方式。

[`runs`用于 JavaScript 操作](#runs-for-javascript-actions)
------------------------------------------------------

**必填**配置操作代码的路径以及用于执行代码的运行时。

### [示例：使用 Node.js v20](#example-using-nodejs-v20)

```
runs:
  using: 'node20'
  main: 'main.js'
```

### [`runs.using`用于 JavaScript 操作](#runsusing-for-javascript-actions)

**必填**用于执行 [`main`](#runsmain) 中指定的代码的运行时。

*   用于 Node.js v20。`node20`

### [`runs.main`](#runsmain)

**必填**包含操作代码的文件。[`using`](#runsusing-for-javascript-actions) 中指定的运行时将执行此文件。

### [`runs.pre`](#runspre)

**自选**允许您在作业开始时，在操作开始之前运行脚本。例如，可用于运行必备组件脚本。使用 [`using`](#runsusing-for-javascript-actions) 语法指定的运行时将执行此文件。默认情况下，该操作始终运行，但您可以使用 [`runs.pre-if`](#runspre-if) 覆盖此操作。`main:``pre:``pre:`

在此示例中，该操作运行一个名为：`pre:``setup.js`

```
runs:
  using: 'node20'
  pre: 'setup.js'
  main: 'index.js'
  post: 'cleanup.js'
```

### [`runs.pre-if`](#runspre-if)

**自选**允许您定义操作执行的条件。仅当满足条件时，操作才会运行。如果未设置，则默认为 。在 中，状态检查函数根据作业的状态进行评估，而不是根据操作本身的状态进行评估。`pre:``pre:``pre-if``pre-if``always()``pre-if`

请注意，上下文不可用，因为尚未运行任何步骤。`step`

在此示例中，仅在基于 Linux 的运行器上运行：`cleanup.js`

```
pre: 'cleanup.js'
  pre-if: runner.os == 'linux'
```

### [`runs.post`](#runspost)

**自选**允许您在操作完成后在作业结束时运行脚本。例如，您可以使用终止某些进程或删除不需要的文件。使用 [`using`](#runsusing-for-javascript-actions) 语法指定的运行时将执行此文件。`main:``post:`

在此示例中，该操作运行一个名为：`post:``cleanup.js`

```
runs:
  using: 'node20'
  main: 'index.js'
  post: 'cleanup.js'
```

默认情况下，该操作始终运行，但您可以使用 覆盖此操作。`post:``post-if`

### [`runs.post-if`](#runspost-if)

**自选**允许您定义操作执行的条件。仅当满足条件时，操作才会运行。如果未设置，则默认为 。在 中，状态检查函数根据作业的状态进行评估，而不是根据操作本身的状态进行评估。`post:``post:``post-if``post-if``always()``post-if`

例如，这将仅在基于 Linux 的运行器上运行：`cleanup.js`

```
post: 'cleanup.js'
  post-if: runner.os == 'linux'
```

[`runs`对于复合操作](#runs-for-composite-actions)
-------------------------------------------

**必填**配置复合操作的路径。

### [`runs.using`对于复合操作](#runsusing-for-composite-actions)

**必填**必须将此值设置为 。`'composite'`

### [`runs.steps`](#runssteps)

**必填**您计划在此操作中运行的步骤。这些可以是步骤或步骤。`run``uses`

#### [`runs.steps[*].run`](#runsstepsrun)

**自选**要运行的命令。这可以是内联的，也可以是操作存储库中的脚本：

```
runs:
  using: "composite"
  steps:
    - run: ${{ github.action_path }}/test/script.sh
      shell: bash
```

或者，您可以使用：`$GITHUB_ACTION_PATH`

```
runs:
  using: "composite"
  steps:
    - run: $GITHUB_ACTION_PATH/script.sh
      shell: bash
```

有关详细信息，请参阅 “[上下文](https://docs.github.com/en/actions/learn-github-actions/contexts#github-context)”。

#### [`runs.steps[*].shell`](#runsstepsshell)

**自选**要运行命令的 shell。您可以使用 “[GitHub Actions 的工作流语法](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idstepsshell)” 中列出的任何 shell。如果已设置，则为必填项。`run`

#### [`runs.steps[*].if`](#runsstepsif)

**自选**除非满足条件，否则可以使用条件来阻止步骤运行。您可以使用任何受支持的上下文和表达式来创建条件。`if`

在条件中使用表达式时，可以选择省略表达式语法，因为 GitHub Actions 会自动将条件计算为表达式。但是，此例外并非适用于所有地方。`if``${{ }}``if`

必须始终使用表达式语法或转义，或者当表达式以 开头时，因为表达式是 YAML 格式的保留表示法。例如：`${{ }}``''``""``()``!``!`

```
if: ${{ ! startsWith(github.ref, 'refs/tags/') }}
```

有关详细信息，请参阅 “[表达式](https://docs.github.com/en/actions/learn-github-actions/expressions)”。

**示例：使用上下文**

仅当事件类型为 a 且事件操作为 时，此步骤才会运行。`pull_request``unassigned`

```
steps:
  - run: echo This event is a pull request that had an assignee removed.
    if: ${{ github.event_name == 'pull_request' && github.event.action == 'unassigned' }}
```

**示例：使用状态检查功能**

仅当复合操作的上一步失败时才运行。有关详细信息，请参阅 “[表达式](https://docs.github.com/en/actions/learn-github-actions/expressions#status-check-functions)”。`my backup step`

```
steps:
  - name: My first step
    uses: octo-org/action-name@main
  - name: My backup step
    if: ${{ failure() }}
    uses: actions/heroku@1.0.0
```

#### [`runs.steps[*].name`](#runsstepsname)

**自选**复合步骤的名称。

#### [`runs.steps[*].id`](#runsstepsid)

**自选**步骤的唯一标识符。您可以使用 在上下文中引用步骤。有关详细信息，请参阅 “[上下文](https://docs.github.com/en/actions/learn-github-actions/contexts)”。`id`

#### [`runs.steps[*].env`](#runsstepsenv)

**自选**仅为该步骤设置环境变量。如果要修改工作流中存储的环境变量，请在复合步骤中使用。`map``echo "{name}={value}" >> $GITHUB_ENV`

#### [`runs.steps[*].working-directory`](#runsstepsworking-directory)

**自选**指定运行命令的工作目录。

#### [`runs.steps[*].uses`](#runsstepsuses)

**自选**选择要在作业中的步骤中运行的操作。操作是可重用的代码单元。可以使用在与工作流相同的存储库、公共存储库或[已发布的 Docker 容器映像](https://hub.docker.com/)中定义的操作。

强烈建议通过指定 Git ref、SHA 或 Docker 标记号来包含正在使用的操作版本。如果未指定版本，则可能会在操作所有者发布更新时中断工作流或导致意外行为。

*   使用已发布操作版本的提交 SHA 对于稳定性和安全性来说是最安全的。
*   使用特定的主要操作版本可以接收关键修复程序和安全补丁，同时仍保持兼容性。它还确保您的工作流程仍然正常工作。
*   使用操作的默认分支可能很方便，但如果有人发布了具有重大更改的新主要版本，则您的工作流可能会中断。

某些操作需要必须使用 [`with`](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions#jobsjob_idstepswith) 关键字设置的输入。查看操作的 README 文件以确定所需的输入。

```
runs:
  using: "composite"
  steps:
    # Reference a specific commit
    - uses: actions/checkout@8f4b7f84864484a7bf31766abe9204da3cbe65b3
    # Reference the major version of a release
    - uses: actions/checkout@v4
    # Reference a specific version
    - uses: actions/checkout@v4.2.0
    # Reference a branch
    - uses: actions/checkout@main
    # References a subdirectory in a public GitHub repository at a specific branch, ref, or SHA
    - uses: actions/aws/ec2@main
    # References a local action
    - uses: ./.github/actions/my-action
    # References a docker public registry action
    - uses: docker://gcr.io/cloud-builders/gradle
    # Reference a docker image published on docker hub
    - uses: docker://alpine:3.8
```

#### [`runs.steps[*].with`](#runsstepswith)

**自选**操作定义的输入参数的 A。每个输入参数都是一个键 / 值对。有关更多信息，请参阅[示例：指定输入](#example-specifying-inputs)。`map`

```
runs:
  using: "composite"
  steps:
    - name: My first step
      uses: actions/hello_world@main
      with:
        first_name: Mona
        middle_name: The
        last_name: Octocat
```

[`runs`用于 Docker 容器操作](#runs-for-docker-container-actions)
----------------------------------------------------------

**必填**配置用于 Docker 容器操作的映像。

### [示例：在存储库中使用 Dockerfile](#example-using-a-dockerfile-in-your-repository)

```
runs:
  using: 'docker'
  image: 'Dockerfile'
```

### [示例：使用公共 Docker 注册表容器](#example-using-public-docker-registry-container)

```
runs:
  using: 'docker'
  image: 'docker://debian:stretch-slim'
```

### [`runs.using`用于 Docker 容器操作](#runsusing-for-docker-container-actions)

**必填**必须将此值设置为 。`'docker'`

### [`runs.pre-entrypoint`](#runspre-entrypoint)

**自选**允许您在操作开始之前运行脚本。例如，可用于运行必备组件脚本。GitHub Actions 用于启动此操作，并在使用相同基础映像的新容器中运行脚本。这意味着运行时状态与主容器不同，并且必须在工作区中访问所需的任何状态，或者作为变量访问。默认情况下，该操作始终运行，但您可以使用 [`runs.pre-if`](#runspre-if) 覆盖此操作。`entrypoint``pre-entrypoint:``docker run``entrypoint``HOME``STATE_``pre-entrypoint:`

使用 [`using`](#runsusing-for-docker-container-actions) 语法指定的运行时将执行此文件。

在此示例中，该操作运行一个名为：`pre-entrypoint:``setup.sh`

```
runs:
  using: 'docker'
  image: 'Dockerfile'
  args:
    - 'bzz'
  pre-entrypoint: 'setup.sh'
  entrypoint: 'main.sh'
```

### [`runs.image`](#runsimage)

**必填**要用作运行操作的容器的 Docker 映像。该值可以是 Docker 基本映像名称、存储库中的本地映像，也可以是 Docker Hub 或其他注册表中的公共映像。若要将本地文件引用到存储库，必须命名该文件，并且必须使用相对于操作元数据文件的路径。应用程序将执行此文件。`Dockerfile``Dockerfile``Dockerfile``docker`

### [`runs.env`](#runsenv)

**自选**指定要在容器环境中设置的环境变量的键 / 值映射。

### [`runs.entrypoint`](#runsentrypoint)

**自选**覆盖 中的 Docker，如果尚未指定，则设置它。当 未指定或您想要覆盖指令时使用。如果省略 ，则将执行您在 Docker 指令中指定的命令。Docker 指令具有 _shell_ 形式和 _exec_ 形式。Docker 文档建议使用指令的 _exec_ 形式。`ENTRYPOINT``Dockerfile``entrypoint``Dockerfile``ENTRYPOINT``ENTRYPOINT``entrypoint``ENTRYPOINT``ENTRYPOINT``ENTRYPOINT``ENTRYPOINT`

有关如何执行的详细信息，请参阅 “[对 GitHub Actions 的 Dockerfile 支持](https://docs.github.com/en/actions/creating-actions/dockerfile-support-for-github-actions#entrypoint)”。`entrypoint`

### [`runs.post-entrypoint`](#runspost-entrypoint)

**自选**允许您在操作完成后运行清理脚本。GitHub Actions 用于启动此操作。由于 GitHub Actions 使用相同的基础映像在新容器中运行脚本，因此运行时状态与主容器不同。您可以在工作区中访问所需的任何状态，也可以以变量的形式访问。默认情况下，该操作始终运行，但您可以使用 [`runs.post-if`](#runspost-if) 覆盖它。`runs.entrypoint``docker run``entrypoint``HOME``STATE_``post-entrypoint:`

```
runs:
  using: 'docker'
  image: 'Dockerfile'
  args:
    - 'bzz'
  entrypoint: 'main.sh'
  post-entrypoint: 'cleanup.sh'
```

### [`runs.args`](#runsargs)

**自选**定义 Docker 容器输入的字符串数组。输入可以包含硬编码字符串。GitHub 在容器启动时将 传递给容器。`args``ENTRYPOINT`

用于代替 . 如果您在 中使用 ，请使用按偏好排序的准则：`args``CMD``Dockerfile``CMD``Dockerfile`

1.  在操作的自述文件中记录所需的参数，并从指令中省略它们。`CMD`
2.  使用允许使用操作而不指定任何 .`args`
3.  如果操作公开了标志或类似内容，请使用它来使操作自记录。`--help`

如果需要将环境变量传递到操作中，请确保操作运行命令行界面以执行变量替换。例如，如果属性设置为 ，则将在命令 shell 中运行。或者，如果您使用 an 运行相同的命令 （），则将在命令 shell 中执行。`entrypoint``"sh -c"``args``Dockerfile``ENTRYPOINT``"sh -c"``args`

有关将该指令用于 GitHub Actions 的详细信息，请参阅 “[GitHub Actions 的 Dockerfile 支持](https://docs.github.com/en/actions/creating-actions/dockerfile-support-for-github-actions#cmd)”。`CMD`

#### [示例：定义 Docker 容器的参数](#example-defining-arguments-for-the-docker-container)

```
runs:
  using: 'docker'
  image: 'Dockerfile'
  args:
    - ${{ inputs.greeting }}
    - 'foo'
    - 'bar'
```

[`branding`](#branding)
-----------------------

**自选**您可以使用颜色和[羽毛](https://feathericons.com/)图标来创建徽章，以个性化和区分您的操作。徽章显示在 [GitHub Marketplace](https://github.com/marketplace?type=actions) 中的操作名称旁边。

### [示例：为操作配置品牌](#example-configuring-branding-for-an-action)

```
branding:
  icon: 'award'
  color: 'green'
```

### [`branding.color`](#brandingcolor)

徽章的背景颜色。可以是以下之一：、、、或 。`white``yellow``blue``green``orange``red``purple``gray-dark`

### [`branding.icon`](#brandingicon)

要使用的 v4.28.0 [羽毛](https://feathericons.com/)图标的名称。

