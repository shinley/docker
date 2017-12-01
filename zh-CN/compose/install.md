---
description: How to install Docker Compose
keywords: compose, orchestration, install, installation, docker, documentation
title: Install Docker Compose
toc_max: 2
---
You can run Compose on macOS, Windows, and 64-bit Linux.

## Prerequisites

Docker Compose relies on Docker Engine for any meaningful work, so make sure you have Docker Engine installed either locally or remote, depending on your setup.

- On desktop systems like Docker for Mac and Windows, Docker Compose is included as part of those desktop installs.

- On Linux systems, first install the [Docker](/engine/installation/index.md#server){: target="*blank" class="*"} for your OS as described on the Get Docker page, then come back here for instructions on installing Compose on Linux systems.

## Install Compose

Follow the instructions below to install Compose on Mac, Windows, Windows Server 2016, or Linux systems, or find out about alternatives like using the `pip` Python package manager or installing Compose as a container.

<ul class="nav nav-tabs">
  
<li class="active"><a data-toggle="tab" data-target="#macOS">Mac</a></li>
<li><a data-toggle="tab" data-target="#windows">Windows</a></li>
<li><a data-toggle="tab" data-target="#linux">Linux</a></li>
<li><a data-toggle="tab" data-target="#alternatives">Alternative Install Options</a></li>
</ul>

<div class="tab-content">
  <div id="macOS" class="tab-pane fade in active">
    <h3>
      Install Compose on macOS
    </h3>
    
    <p>
      <strong>Docker for Mac</strong> and <strong>Docker Toolbox</strong> already include Compose along with other Docker apps, so Mac users do not need to install Compose separately. Docker install instructions for these are here:
    </p>
    
    <ul>
      <li>
        <a href="/docker-for-mac/install.md">Get Docker for Mac</a>
      </li>
      <li>
        <a href="/toolbox/overview.md">Get Docker Toolbox</a> (for older systems)
      </li>
    </ul>
    
    <hr />
  </div>
  
  <div id="windows" class="tab-pane fade">
    <h3>
      Install Compose on Windows systems
    </h3>
    
    <p>
      <strong>Docker for Windows</strong> and <strong>Docker Toolbox</strong> already include Compose along with other Docker apps, so most Windows users do not need to install Compose separately. Docker install instructions for these are here:
    </p>
    
    <ul>
      <li>
        <a href="/docker-for-windows/install.md">Get Docker for Windows</a>
      </li>
      <li>
        <a href="/toolbox/overview.md">Get Docker Toolbox</a> (for older systems)
      </li>
    </ul>
    
    <p>
      <strong>If you are running the Docker daemon and client directly on Microsoft Windows Server 2016</strong> (with <a href="/engine/installation/windows/docker-ee.md">Docker EE for Windows Server 2016</a>, you <em>do</em> need to install Docker Compose. To do so, follow these steps:
    </p>
    
    <ol>
      <li>
        <p>
          Start an "elevated" PowerShell (run it as administrator). Search for PowerShell, right-click, and choose <strong>Run as administrator</strong>. When asked if you want to allow this app to make changes to your device, click <strong>Yes</strong>.
        </p>
        <p>
          In PowerShell, run the following command to download Docker Compose, replacing <code>$dockerComposeVersion</code> with the specific version of Compose you want to use:
        </p>
        <pre><code class="none">Invoke-WebRequest "https://github.com/docker/compose/releases/download/$dockerComposeVersion/docker-compose-Windows-x86_64.exe" -UseBasicParsing -OutFile $Env:ProgramFiles\docker\docker-compose.exe
</code></pre>
        <p>
          For example, to download Compose version {{site.compose_version}}, the command is:
        </p>
        <pre><code class="none">Invoke-WebRequest "https://github.com/docker/compose/releases/download/{{site.compose_version}}/docker-compose-Windows-x86_64.exe" -UseBasicParsing -OutFile $Env:ProgramFiles\docker\docker-compose.exe
</code></pre>
        <blockquote>
          <p>
            Use the latest Compose release number in the download command.
          </p>
          
          <p>
            As already mentioned, the above command is an <em>example</em>, and it may become out-of-date once in a while. Always follow the command pattern shown above it. If you cut-and-paste an example, check which release it specifies and, if needed, replace <code>$dockerComposeVersion</code> with the release number that you want. Compose releases are also available for direct download on the <a href="https://github.com/docker/compose/releases">Compose repository release page on GitHub</a>{:target="<em>blank" class="</em>"}. {: .important}
          </p>
        </blockquote>
      </li>
      
      <li>
        <p>
          Run the executable to install Compose.
        </p>
      </li>
    </ol>
    
    <hr />
  </div>
  
  <div id="linux" class="tab-pane fade">
    <h3>
      Install Compose on Linux systems
    </h3>
    
    <p>
      On <strong>Linux</strong>, you can download the Docker Compose binary from the <a href="https://github.com/docker/compose/releases">Compose repository release page on GitHub</a>{: target="<em>blank" class="</em>"}. Follow the instructions from the link, which involve running the <code>curl</code> command in your terminal to download the binaries. These step by step instructions are also included below.
    </p>
    
    <ol>
      <li>
        <p>
          Run this command to download the latest version of Docker Compose:
        </p>
        <pre><code class="bash">sudo curl -L https://github.com/docker/compose/releases/download/{{site.compose_version}}/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
</code></pre>
        <blockquote>
          <p>
            Use the latest Compose release number in the download command.
          </p>
          
          <p>
            The above command is an <em>example</em>, and it may become out-of-date. To ensure you have the latest version, check the <a href="https://github.com/docker/compose/releases">Compose repository release page on GitHub</a>{: target="<em>blank" class="</em>"}. {: .important}
          </p>
        </blockquote>
        
        <p>
          If you have problems installing with <code>curl</code>, see <a href="install.md#alternative-install-options">Alternative Install Options</a>.
        </p>
      </li>
      
      <li>
        <p>
          Apply executable permissions to the binary:
        </p>
        <pre><code class="bash">sudo chmod +x /usr/local/bin/docker-compose
</code></pre>
      </li>
      
      <li>
        <p>
          Optionally, install <a href="completion.md">command completion</a> for the <code>bash</code> and <code>zsh</code> shell.
        </p>
      </li>
      
      <li>
        <p>
          Test the installation.
        </p>
        <pre><code class="bash">$ docker-compose --version
docker-compose version {{site.compose_version}}, build 1719ceb
</code></pre>
      </li>
    </ol>
    
    <hr />
  </div>
  
  <div id="alternatives" class="tab-pane fade">
    <h3>
      Alternative install options
    </h3>
    
    <ul>
      <li>
        <a href="#install-using-pip">Install using pip</a>
      </li>
      <li>
        <a href="#install-as-a-container">Install as a container</a>
      </li>
    </ul>
    
    <h4>
      Install using pip
    </h4>
    
    <p>
      Compose can be installed from <a href="https://pypi.python.org/pypi/docker-compose">pypi</a> using <code>pip</code>. If you install using <code>pip</code>, we recommend that you use a <a href="https://virtualenv.pypa.io/en/latest/">virtualenv</a> because many operating systems have python system packages that conflict with docker-compose dependencies. See the <a href="http://docs.python-guide.org/en/latest/dev/virtualenvs/">virtualenv tutorial</a> to get started.
    </p>
    
    <pre><code class="bash">pip install docker-compose
</code></pre>
    
    <p>
      If you are not using virtualenv,
    </p>
    
    <pre><code class="bash">sudo pip install docker-compose
</code></pre>
    
    <blockquote>
      <p>
        pip version 6.0 or greater is required.
      </p>
    </blockquote>
    
    <h4>
      Install as a container
    </h4>
    
    <p>
      Compose can also be run inside a container, from a small bash script wrapper. To install compose as a container run this command. Be sure to replace the version number with the one that you want, if this example is out-of-date:
    </p>
    
    <pre><code class="bash">$ sudo curl -L --fail https://github.com/docker/compose/releases/download/{{site.compose_version}}/run.sh -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
</code></pre>
    
    <blockquote>
      <p>
        Use the latest Compose release number in the download command.
      </p>
      
      <p>
        The above command is an <em>example</em>, and it may become out-of-date once in a while. Check which release it specifies and, if needed, replace the given release number with the one that you want. Compose releases are also listed and available for direct download on the <a href="https://github.com/docker/compose/releases">Compose repository release page on GitHub</a>{: target="<em>blank" class="</em>"}. {: .important}
      </p>
    </blockquote>
    
    <hr />
  </div>
</div>

## Master builds

If you're interested in trying out a pre-release build, you can download a binary from <https://dl.bintray.com/docker-compose/master/>. Pre-release builds allow you to try out new features before they are released, but may be less stable.

## Upgrading

If you're upgrading from Compose 1.2 or earlier, you'll need to remove or migrate your existing containers after upgrading Compose. This is because, as of version 1.3, Compose uses Docker labels to keep track of containers, and so they need to be recreated with labels added.

If Compose detects containers that were created without labels, it will refuse to run so that you don't end up with two sets of them. If you want to keep using your existing containers (for example, because they have data volumes you want to preserve), you can use Compose 1.5.x to migrate them with the following command:

```bash
docker-compose migrate-to-labels
```

Alternatively, if you're not worried about keeping them, you can remove them. Compose will just create new ones.

```bash
docker rm -f -v myapp_web_1 myapp_db_1 ...
```

## Uninstallation

To uninstall Docker Compose if you installed using `curl`:

```bash
sudo rm /usr/local/bin/docker-compose
```

To uninstall Docker Compose if you installed using `pip`:

```bash
pip uninstall docker-compose
```

> Got a "Permission denied" error?
> 
> If you get a "Permission denied" error using either of the above methods, you probably do not have the proper permissions to remove `docker-compose`. To force the removal, prepend `sudo` to either of the above commands and run again.

## Where to go next

- [User guide](index.md)
- [Getting Started](gettingstarted.md)
- [Get started with Django](django.md)
- [Get started with Rails](rails.md)
- [Get started with WordPress](wordpress.md)
- [Command line reference](/compose/reference/index.md)
- [Compose file reference](compose-file.md)