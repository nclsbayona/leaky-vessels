<h1>Leaky Vessels vulnerabilities</h1>

<details name="section">
<summary><h2>Contents</h2></summary>
  <ol>
    <li>Definition (What is Leaky Vessels?)</li>
    <li>Importance (Why is knowing about Leaky Vessels important?)</li>
    <li>
      <details name="section-vulnerabilities">
        <summary>Explanation of each vulnerability (Names taken from <a href="https://github.com/snyk/leaky-vessels-dynamic-detector">leaky-vessels-dynamic-detector</a>)</summary>
        <ol>
          <li>runc process.cwd & Leaked fds Container Breakout [CVE-2024-21626]</li>
          <li>Buildkit Mount Cache Race: Build-time Race Condition Container Breakout [CVE-2024-23651]</li>
          <li>Buildkit GRPC SecurityMode Privilege Check [CVE-2024-23653]</li>
          <li>Buildkit Build-time Container Teardown Arbitrary Delete [CVE-2024-23652]</li>
        </ol>
      </details>
    </li>
    <li>Mitigations (What can I do?)</li>
  </ol>
</details>

<hr />

<details name="section">
  <summary><h3>Definition (What is Leaky Vessels?)</h3></summary>
  <div>
    Leaky Vessels is the name given to a set of vulnerabilities discovered and reported by Snyk on 2023 but publically-listed on January 31, 2024. This set of vulnerabilities allow an attacker to escape a containerized environment and is made-uo of four vulnerabilities that target different parts of the docker architecture. <img src="https://i.stack.imgur.com/lAtSR.png" />
  </div>
  <br />
</details>

<details name="section">
  <summary><h3>Importance (Why is knowing about Leaky Vessels important?)</h3></summary>
  <div>
    Knowing about Leaky Vessels vulnerabilities is important because Containers are a technology used frequently on the Industry and getting to know threats you might face allow you to prepare better than someone that is just unaware of what can actually happen.
  </div>
  <br />
</details>

<details name="section">
  <summary><h3>Explanation of each vulnerability (Names taken from <a href="https://github.com/snyk/leaky-vessels-dynamic-detector">leaky-vessels-dynamic-detector</a>)</h3></summary>
    <ol>
      <li>
        <details name="section-vulnerabilities">
          <summary><h4>runc process.cwd & Leaked fds Container Breakout [CVE-2024-21626]</h4></summary>
          Manipulation of a newly spawned process' current working directory (process.cwd). This uses a file descriptor (https://www.golinuxcloud.com/linux-file-descriptors/) leak that allows an attacker to have a working directory in the host filesystem namespace (An fd is open on the current working directory so it can be used to escape a containerized environment.
          <br />
        </details>
      </li>
      <li>
        <details name="section-vulnerabilities">
          <summary><h4>Buildkit Mount Cache Race: Build-time Race Condition Container Breakout [CVE-2024-23651]</h4></summary>
          <br />
        </details>
      </li>
      <li>
        <details name="section-vulnerabilities">
          <summary><h4>Buildkit GRPC SecurityMode Privilege Check [CVE-2024-23653]</h4></summary>
          <br />
        </details>
      </li>
      <li>
        <details name="section-vulnerabilities">
          <summary><h4>Buildkit Build-time Container Teardown Arbitrary Delete [CVE-2024-23652]</h4></summary>
        </details>
      </li>
    </ol>
  <br />
</details>

<details name="section">
  <summary><h3>Mitigations (What can I do?)</h3></summary>
  <br />
</details>
