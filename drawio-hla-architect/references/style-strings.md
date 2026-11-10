# Enterprise style strings

Read this file when writing pod, database, icon, or edge style attributes. Copy the style string verbatim; the connection-point array, `html=1;`, and the lifecycle colours are load-bearing.

### Kubernetes Pods with Mandatory Connection Points
```xml
<!-- New Microservice (#03CCFF) -->
style="sketch=0;html=1;dashed=0;whitespace=wrap;fillColor=#dae8fc;strokeColor=#03CCFF;strokeWidth=2;points=[[0.005,0.63,0],[0.1,0.2,0],[0.9,0.2,0],[0.5,0,0],[0.995,0.63,0],[0.72,0.99,0],[0.5,1,0],[0.28,0.99,0]];verticalLabelPosition=bottom;align=center;verticalAlign=top;shape=mxgraph.kubernetes.icon;prIcon=pod;fontSize=10;fontStyle=1;fontColor=#000000;"

<!-- Enhanced Microservice (#92D14F) -->
style="sketch=0;html=1;dashed=0;whitespace=wrap;fillColor=#d5e8d4;strokeColor=#92D14F;strokeWidth=2;points=[[0.005,0.63,0],[0.1,0.2,0],[0.9,0.2,0],[0.5,0,0],[0.995,0.63,0],[0.72,0.99,0],[0.5,1,0],[0.28,0.99,0]];verticalLabelPosition=bottom;align=center;verticalAlign=top;shape=mxgraph.kubernetes.icon;prIcon=pod;fontSize=10;fontStyle=1;fontColor=#000000;"

<!-- Existing / Reused Microservice (#BFBFBF) -->
style="sketch=0;html=1;dashed=0;whitespace=wrap;fillColor=#f5f5f5;strokeColor=#BFBFBF;strokeWidth=1.5;points=[[0.005,0.63,0],[0.1,0.2,0],[0.9,0.2,0],[0.5,0,0],[0.995,0.63,0],[0.72,0.99,0],[0.5,1,0],[0.28,0.99,0]];verticalLabelPosition=bottom;align=center;verticalAlign=top;shape=mxgraph.kubernetes.icon;prIcon=pod;fontSize=10;fontStyle=1;fontColor=#000000;"

<!-- External Microservice / 3rd Party (#EF7D30) -->
style="sketch=0;html=1;dashed=0;whitespace=wrap;fillColor=#ffe6cc;strokeColor=#EF7D30;strokeWidth=1.5;points=[[0.005,0.63,0],[0.1,0.2,0],[0.9,0.2,0],[0.5,0,0],[0.995,0.63,0],[0.72,0.99,0],[0.5,1,0],[0.28,0.99,0]];verticalLabelPosition=bottom;align=center;verticalAlign=top;shape=mxgraph.kubernetes.icon;prIcon=pod;fontSize=10;fontStyle=1;fontColor=#000000;"
```

### Standard Infrastructure & Vector Database Icons
```xml
<!-- PostgreSQL Vector SVG Icon (Mandatory html=1;) -->
style="shape=image;html=1;verticalLabelPosition=bottom;labelBackgroundColor=default;verticalAlign=top;aspect=fixed;imageAspect=0;whiteSpace=wrap;image=data:image/svg+xml,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI2NCIgdmlld0JveD0iMCAwIDI1LjYgMjUuNiIgaGVpZ2h0PSI2NCI+PHN0eWxlPi5Ce3N0cm9rZS1saW5lY2FwOnJvdW5kfS5De3N0cm9rZS1saW5lam9pbjpyb3VuZH0uRHtzdHJva2UtbGluZWpvaW46bWl0ZXJ9LkV7c3Ryb2tlLXdpZHRoOi43MTZ9PC9zdHlsZT48ZyBzdHJva2U9IiNmZmYiIGZpbGw9Im5vbmUiPjxwYXRoIGNsYXNzPSJEIiBzdHJva2Utd2lkdGg9IjIuMTQ5IiBzdHJva2UtbGluZWNhcD0iYnV0dCIgc3Ryb2tlPSIjMDAwIiBmaWxsPSIjMDAwIiBkPSJNMTguOTgzIDE4LjYzNmMuMTYzLTEuMzU3LjExNC0xLjU1NSAxLjEyNC0xLjMzNmwuMjU3LjAyM2MuNzc3LjAzNSAxLjc5My0uMTI1IDIuNC0uNDAyIDEuMjg1LS41OTYgMi4wNDctMS41OTIuNzgtMS4zMy0yLjg5LjU5Ni0zLjEtLjM4My0zLjEtLjM4MyAzLjA1My00LjUzIDQuMzMtMTAuMjggMy4yMjctMTEuNjg3LTMuMDA0LTMuODQtOC4yMDUtMi4wMjQtOC4yOTItMS45NzVsLS4wMjguMDA1Yy0uNTctLjEyLTEuMi0uMTktMS45My0uMi0xLjMwOC0uMDItMi4zLjM0My0zLjA1NC45MTQgMCAwLTkuMjc3LTMuODIyLTguODQ2IDQuODA3LjA5MiAxLjgzNiAyLjYzIDEzLjkgNS42NiAxMC4yNUM4LjI5IDE1Ljk4NyA5LjM2IDE0Ljg2IDkuMzYgMTQuODZjLjUzLjM1MyAxLjE2Ny41MzMgMS44MzQuNDY4bC4wNTItLjA0NGEyLjAxIDIuMDEgMCAwIDAgLjAyMS41MThjLS43OC44NzItLjU1IDEuMDI1LTIuMTEgMS4zNDYtMS41NzguMzI1LS42NS45MDQtLjA0NiAxLjA1Ni43MzQuMTg0IDIuNDMyLjQ0NCAzLjU4LTEuMTYybC0uMDQ2LjE4M2MuMzA2LjI0NS4yODUgMS43Ni4zMyAyLjg0MnMuMTE2IDIuMDkzLjMzNyAyLjY4OC40OCAyLjEzIDIuNTMgMS43YzEuNzEzLS4zNjcgMy4wMjMtLjg5NiAzLjE0My01LjgxIi8+PHBhdGggc3Ryb2tlPSJub25lIiBmaWxsPSIjMzM2NzkxIiBkPSJNMjMuNTM1IDE1LjZjLTIuODkuNTk2LTMuMS0uMzgzLTMuMS0uMzgzIDMuMDUzLTQuNTMgNC4zMy0xMC4yOCAzLjIyOC0xMS42ODctMy4wMDQtMy44NC04LjIwNS0yLjAyMy04LjI5Mi0xLjk3NmwtLjAyOC4wMDVhMTAuMzEgMTAuMzEgMCAwIDAtMS45MjktLjIwMWMtMS4zMDgtLjAyLTIuMy4zNDMtMy4wNTQuOTE0IDAgMC05LjI3OC0zLjgyMi04Ljg0NiA0LjgwNy4wOTIgMS44MzYgMi42MyAxMy45IDUuNjYgMTAuMjVDOC4yOSAxNS45ODcgOS4zNiAxNC44NiA5LjM2IDE0Ljg2Yy41My4zNTMgMS4xNjcuNTMzIDEuODM0LjQ2OGwuMDUyLS4wNDRhMi4wMiAyLjAyIDAgMCAwIC4wMjEuNTE4Yy0uNzguODcyLS41NSAxLjAyNS0yLjExIDEuMzQ2LTEuNTc4LjMyNS0uNjUuOTA0LS4wNDYgMS4wNTYuNzM0LjE4NCAyLjQzMi40NDQgMy41OC0xLjE2MmwtLjA0Ni4xODNjLjMwNi4yNDUuNTIgMS41OTMuNDg0IDIuODE1cy0uMDYgMi4wNi4xOCAyLjcxNi40OCAyLjEzIDIuNTMgMS43YzEuNzEzLS4zNjcgMi42LTEuMzIgMi43MjUtMi45MDYuMDg4LTEuMTI4LjI4Ni0uOTYyLjMtMS45N2wuMTYtLjQ3OGMuMTgzLTEuNTMuMDMtMi4wMjMgMS4wODUtMS43OTNsLjI1Ny4wMjNjLjc3Ny4wMzUgMS43OTQtLjEyNSAyLjM5LS40MDIgMS4yODUtLjU5NiAyLjA0Ny0xLjU5Mi43OC0xLjMzeiIvPjxnIGNsYXNzPSJFIj48ZyBjbGFzcz0iQiI+PHBhdGggY2xhc3M9IkMiIGQ9Ik0xMi44MTQgMTYuNDY3Yy0uMDggMi44NDYuMDIgNS43MTIuMjk4IDYuNHMuODc1IDIuMDUgMi45MjYgMS42MTJjMS43MTMtLjM2NyAyLjMzNy0xLjA3OCAyLjYwNy0yLjY0N2wuNjMzLTUuMDE3TTEwLjM1NiAyLjJTMS4wNzItMS41OTYgMS41MDQgNy4wMzNjLjA5MiAxLjgzNiAyLjYzIDEzLjkgNS42NiAxMC4yNUM4LjI3IDE1Ljk1IDkuMjcgMTQuOTA3IDkuMjcgMTQuOTA3bTYuMS0xMy40Yy0uMzIuMSA1LjE2NC0yLjAwNSA4LjI4MiAxLjk3OCAxLjEgMS40MDctLjE3NSA3LjE1Ny0zLjIyOCAxMS42ODciLz48cGF0aCBzdHJva2UtbGluZWpvaW49ImJldmVsIiBkPSJNMjAuNDI1IDE1LjE3cy4yLjk4IDMuMS4zODJjMS4yNjctLjI2Mi41MDQuNzM0LS43OCAxLjMzLTEuMDU0LjQ5LTMuNDE4LjYxNS0zLjQ1Ny0uMDYtLjEtMS43NDUgMS4yNDQtMS4yMTUgMS4xNDctMS42NTItLjA4OC0uMzk0LS42OS0uNzgtMS4wODYtMS43NDQtLjM0Ny0uODQtNC43Ni03LjI5IDEuMjI0LTYuMzMzLjIyLS4wNDUtMS41Ni01LjctNy4xNi01Ljc4MlM3Ljk5IDguMTk2IDcuOTkgOC4xOTYiLz48L2c+PGcgY2xhc3M9IkMiPjxwYXRoIGQ9Ik0xMS4yNDcgMTUuNzY4Yy0uNzguODcyLS41NSAxLjAyNS0yLjExIDEuMzQ2LTEuNTc4LjMyNS0uNjUuOTA0LS4wNDYgMS4wNTYuNzM0LjE4NCAyLjQzMi40NDQgMy41OC0xLjE2My4zNS0uNDktLjAwMi0xLjI3LS40ODItMS40NjgtLjIzMi0uMDk2LS41NDItLjIxNi0uOTQuMjN6Ii8+PHBhdGggY2xhc3M9IkIiIGQ9Ik0xMS4xOTYgMTUuNzUzYy0uMDgtLjUxMy4xNjgtMS4xMjIuNDMzLTEuODM2LjM5OC0xLjA3IDEuMzE2LTIuMTQuNTgyLTUuNTM3LS41NDctMi41My00LjIyLS41MjctNC4yMi0uMTg0cy4xNjYgMS43NC0uMDYgMy4zNjVjLS4yOTcgMi4xMjIgMS4zNSAzLjkxNiAzLjI0NiAzLjczMyIvPjwvZz48L2c+PGcgY2xhc3M9IkQiIGZpbGw9IiNmZmYiPjxwYXRoIHN0cm9rZS13aWR0aD0iLjIzOSIgZD0iTTEwLjMyMiA4LjE0NWMtLjAxNy4xMTcuMjE1LjQzLjUxNi40NzJzLjU1OC0uMjAyLjU3NS0uMzItLjIxNS0uMjQ2LS41MTYtLjI4OC0uNTYuMDItLjU3NS4xMzZ6Ii8+PHBhdGggc3Ryb2tlLXdpZHRoPSIuMTE5IiBkPSJNMTkuNDg2IDcuOTA2Yy4wMTYuMTE3LS4yMTUuNDMtLjUxNi40NzJzLS41Ni0uMjAyLS41NzUtLjMyLjIxNS0uMjQ2LjUxNi0uMjg4LjU2LjAyLjU3NS4xMzZ6Ii8+PC9nPjxwYXRoIGNsYXNzPSJCIEMgRSIgZD0iTTIwLjU2MiA3LjA5NWMuMDUuOTItLjE5OCAxLjU0NS0uMjMgMi41MjQtLjA0NiAxLjQyMi42NzggMy4wNS0uNDEzIDQuNjgiLz48L2c+PC9zdmc+;fontSize=10;fontStyle=1;align=center;"

<!-- Redis Cache Snapcraft Icon -->
style="shape=image;html=1;verticalLabelPosition=bottom;labelBackgroundColor=default;verticalAlign=top;aspect=fixed;imageAspect=0;whiteSpace=wrap;image=https://dashboard.snapcraft.io/site_media/appmedia/2020/08/1529926.png;fontSize=10;fontStyle=1;align=center;strokeWidth=1;fillColor=none;"

<!-- Kong API Gateway Icon (Embedded Vector SVG - 100% Offline & Reliable) -->
style="shape=image;html=1;verticalLabelPosition=bottom;labelBackgroundColor=default;verticalAlign=top;aspect=fixed;imageAspect=0;whiteSpace=wrap;image=data:image/svg+xml,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNTMgMTM3IiB3aWR0aD0iNjQiIGhlaWdodD0iNjQiPgogIDxwYXRoIGZpbGw9IiMwMDJBM0EiIGQ9Ik01MC41LDExMi45bC0zLjcsNC43LDguNCwxMy4yLS45LDYuMWgzNS42bDIuNS02LjEtMTQuMy0xNy45aC0yNy42WiIvPgogIDxwYXRoIGZpbGw9IiMwMDdBQzIiIGQ9Ik02OS45LDMyLjZsLTEyLjksMjIuNyw2Mi45LDc0LjgtMS44LDYuOWgyOC44bDUuMi0yNC4zTDg0LjksMzIuNWgtMTVaIi8+CiAgPHBhdGggZmlsbD0iIzEyNjRBMyIgZD0iTTc4LjUsMTUuNWwtNi4xLDExLjNoMTUuMmwyNi4xLDMxLjIsMTUuNS0xMi44di04LjFsLTUuNC03LjYsNC00LjJMOTYuNy42bC0xOC4yLDE0LjlaIi8+CiAgPHBhdGggZmlsbD0iIzAwM0I1QyIgZD0iTTMxLjcsNzguN2gtOC41TC44LDEwNy4zdjI5LjZoMjRsNC4yLTUuNSwxOC41LTI0LjFoMjYuOGw4LjMtMTIuNy0yOS4xLTM0LjctMjEuOSwxOC45WiIvPgo8L3N2Zz4=;fontSize=10;fontStyle=1;align=center;"

<!-- Kafka Event Broker Icon -->
style="shape=image;html=1;verticalLabelPosition=bottom;labelBackgroundColor=default;verticalAlign=top;aspect=fixed;imageAspect=0;whiteSpace=wrap;image=https://www.svgrepo.com/show/353951/kafka-icon.svg;fontSize=10;fontStyle=1;align=center;"
```

### Official STD Lifecycle Connectors (Mandatory Arc Jumps & Colors)
Connections must declare exact stroke colors corresponding to the lifecycle state in the STD palette tab:

```xml
<!-- 1. New Connection (#03CCFF) -->
<!-- Sync -->
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;jumpStyle=arc;jumpSize=6;html=1;strokeColor=#03CCFF;strokeWidth=2;endArrow=classic;"
<!-- Async (Animated) -->
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;jumpStyle=arc;jumpSize=6;html=1;dashed=1;flowAnimation=1;strokeColor=#03CCFF;strokeWidth=2;endArrow=classic;"

<!-- 2. Enhanced Connection (#92D14F) -->
<!-- Sync -->
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;jumpStyle=arc;jumpSize=6;html=1;strokeColor=#92D14F;strokeWidth=2;endArrow=classic;"
<!-- Async (Animated) -->
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;jumpStyle=arc;jumpSize=6;html=1;dashed=1;flowAnimation=1;strokeColor=#92D14F;strokeWidth=2;endArrow=classic;"

<!-- 3. Existing / Reused Connection (#BFBFBF) -->
<!-- Sync -->
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;jumpStyle=arc;jumpSize=6;html=1;strokeColor=#BFBFBF;strokeWidth=2;endArrow=classic;"
<!-- Async (Animated) -->
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;jumpStyle=arc;jumpSize=6;html=1;dashed=1;flowAnimation=1;strokeColor=#BFBFBF;strokeWidth=2;endArrow=classic;"

<!-- 4. External Connection (#EF7D30) -->
<!-- Sync -->
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;jumpStyle=arc;jumpSize=6;html=1;strokeColor=#EF7D30;strokeWidth=2;endArrow=classic;"
<!-- Async (Animated) -->
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;jumpStyle=arc;jumpSize=6;html=1;dashed=1;flowAnimation=1;strokeColor=#EF7D30;strokeWidth=2;endArrow=classic;"

<!-- 5. Kafka Event Bus Connection (#FF6A00) -->
style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;jumpStyle=arc;jumpSize=6;html=1;dashed=1;flowAnimation=1;strokeColor=#FF6A00;strokeWidth=2;endArrow=classic;"
```


---
