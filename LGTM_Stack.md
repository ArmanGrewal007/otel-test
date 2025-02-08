
<table>
  <tr>
    <th><img src="https://icons-theta.vercel.app/icon?i=opentelemetery" />Open Telemetery</th>
    <th><img src="https://icons-theta.vercel.app/icon?i=loki" />Loki</th>
    <th><img src="https://icons-theta.vercel.app/icon?i=grafana" />Grafana</th>
    <th><img src="https://icons-theta.vercel.app/icon?i=tempo" />Tempo</th>
    <th><img src="https://icons-theta.vercel.app/icon?i=prometheus" />Prometheus/<img src="https://icons-theta.vercel.app/icon?i=mimir" />Mimir</th></tr>
  <tr>
    <td>Collects telemetry data (Metrics, Logs and Traces) while being vendor agnostic.</td>
    <td>DB for Logs</td>
    <td>Visualization</td>
    <td>DB for Traces</td>
    <td>Time Series DB for Metrics</td>
  </tr>
</table>

### Collectively it becomes otel-lgtm stack and it has its own Docker image:- https://hub.docker.com/r/grafana/otel-lgtm (Not recommended for prod)
<div align="center"><img src="https://github.com/user-attachments/assets/d1bc95da-34ec-4980-a53d-e0f82e1e30f5" /></div>

<table>
  <thead>
    <tr>
      <th>Data Type</th>
      <th>Description</th>
      <th>Key Characteristics</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Metrics</td>
      <td>
        Quantitative measurements collected over time (e.g., CPU usage, request rates, latency).
      </td>
      <td>
        <ul>
          <li>Aggregated time-series data</li>
          <li>Low cardinality</li>
          <li>Ideal for alerting and trend analysis</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Traces</td>
      <td>
        Detailed records of a single request's path through a distributed system, capturing timing and causal relationships.
      </td>
      <td>
        <ul>
          <li>Span-based representation</li>
          <li>High-cardinality contextual data</li>
          <li>Used for pinpointing performance bottlenecks and debugging</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Logs</td>
      <td>
        Unstructured or semi-structured text records that document events, errors, or other system activities.
      </td>
      <td>
        <ul>
          <li>Granular, verbose information</li>
          <li>Often used for ad-hoc troubleshooting</li>
          <li>Can include high-cardinality details</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>


1. Use [Hostinger](https://www.hostinger.in/) for deployment, they give a relatively cheap linux Virtual Private Server.
2. Choose a docker deployment.
3. Get the ip address and root password and from you local system ssh into that.

Now you need to run an app which will send logs/metrics/traces to this 
- You can build a server with deno, and it will automatically run traces on your server, and will also collect all the console.logs!
- 
