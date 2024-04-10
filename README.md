sequenceDiagram
renderer->>+preload: Read data from file system
preload->>-renderer: Data
renderer->>preload: Maximize window
activate preload
preload-->>main: Invoke IPC command
activate main
main-->>preload: IPC response
deactivate main
preload->>renderer: Window maximized
deactivate preload
