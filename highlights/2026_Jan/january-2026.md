# January 2026 Highlights

## TL;DR
- 🚀 **Order Portal v1 Pilot**: Launched with 11.5% weekly order adoption.
- ⚡ **Performance**: Reduced DB connection load by **~80%** via smart caching.
- 🌏 **Connectivity**: Established **NL-CN Network SD-WAN Bridge** for secure cross-border access.
- 🏗️ **New BE Design**: Kicked off architecture for the scalable Next-Gen User Service.

## Releases
- **Order Portal v1 Pilot**: Successfully launched the Order Portal pilot on Jan 7th to an initial group of 10 installers.
  
  **Pilot Performance**:
  The pilot has seen steady adoption, with the portal's share of weekly orders growing from **2.2% to 11.5%** in just three weeks.
  
  <div style="display: flex; gap: 10px;">
    <div style="flex: 1;">
        <img src="./Order%20Portal%20MAU.png" alt="Monthly and Weekly Sales Order Trends" style="width: 100%;" />
        <p><em>Figure 1: Portal adoption trend showing an increase to 11.5% of total weekly orders.</em></p>
    </div>
    <div style="flex: 1;">
        <img src="./OrderingOverviewENG.png" alt="Order Portal Interface" style="width: 100%;" />
        <p><em>Figure 2: The new streamlined ordering interface for installers.</em></p>
    </div>
  </div>

## Backend Stability Improvements
- **Performance Optimization**: Enhanced backend stability by reducing connection load from BE to DB by **~80%**.
  - **Smart Caching**: Implemented advanced caching for high-traffic data models (`HeatpumpStatus` and `Heatpump`).
  - **Query Optimization**: Eliminated redundant and repetitive read operations in the Heatpump Log service.
  ![Cache improvement](./cache%20improvements.png)

- **Centralized Observability**: Deployed a comprehensive central dashboard for real-time system observability on PostgresDB, BE Application, and Integration services.
  *Future Roadmap: Integration of AI-based anomaly detection for backend application logs.*
  
  <div style="display: flex; gap: 10px; flex-wrap: wrap;">
    <img src="./db%20dashboard.png" width="300" alt="Central Dashboard" />
    <img src="./BE%20Application%20Dashboard.png" width="300" alt="Postgres Dashboard" />
    <img src="./azure%20workbooks.png" width="300" alt="Application Dashboard" />
  </div>

- **Proactive Alerting**: Rolled out new alert mechanisms to detect service bottlenecks and provide early warnings. Alert coverage will be continuously expanded.
  ![Alert System](./alerts.png)

- **Scheduled Releases**: Established a regular release cadence to ensure sufficient stability testing ("bake time") and provide clear, transparent changelogs.
  [View Release Notes](https://teams.microsoft.com/l/message/19:731b6bdc22924e228954485bbf940ce3@thread.tacv2/1767788213154?tenantId=afcb4032-65a3-4bf5-894e-db5aeefe6471&groupId=5f7d0283-3586-4b63-8972-dfa30fcdaa12&parentMessageId=1767788213154&teamName=Weheat&channelName=Software%20Updates&createdTime=1767788213154).

## Infrastructure & Connectivity
- **Global Network Bridge (NL-CN)**: Established an SD-WAN bi-directional connection between Netherlands and China regions. This enables secure cross-border access to private internal tools, such as the [China Purchase Order Management System](https://poms.wf02.wefabricate.cn/) for the NL purchasing team.
## Support & Hotfixes
- **Cross-Version Firmware Support**: Deployed critical hotfixes to enable seamless firmware updates across mixed version environments, significantly aiding Support operations.

## New Initiatives
- **Non-blocking Firmware Update**: Development kicked off in both Firmware and BE teams, with a defined delivery timeline.
  <br><img src="./nonblocking%20fw.png" width="400" alt="Development Progress" />

- **Next-Gen User Service**: Initiated the architectural design phase for the new, scalable Backend User Service.
  <br><img src="./new%20BE%20design.png" width="400" alt="Design Overview" />
