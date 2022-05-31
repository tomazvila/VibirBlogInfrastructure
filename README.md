# VibirBlog Infrastructure
Infrastructure for VibirBlog

# Infrastructure to be made

```
        Ports:                                        
            80◀────┐                                  
           443◀───┐│                                  
            22◀──┐││                                  
                 │││                                  
┌────────────────┼┼┼─────────────────────────────────┐
│ MyHome      ┌──┴┴┴───┐                             │
│         ┌───│ Router │────Port 22───────┐          │
│  Ports: │   └────────┘                  │          │
│      80 │                               ▼          │
│     443 ▼                     ┌───────────────────┐│
│ ┌──────────────┐              │Lenovo x250        ││
│ │Raspberry pi 4│              │Development server ││
│ │  ┌────────┐  │              │┌────────────────┐ ││
│ │  │Traefik │  ◀─dev.vibir.lt─▶│ Ihp web service│ ││
│ │  └────────┘  ◀───────┐      ││ ConyMony blog  │ ││
│ └──────────────┘       │      │└────────────────┘ ││
│                        │      └───────────────────┘│
│                  www.vibir.lt                      │
│                        │      ┌───────────────────┐│
│                        │      │ Acer laptop       ││
│ ┌──────────────┐       │      │ Production server ││
│ │Raspberry pi 4│       │      │┌────────────────┐ ││
│ │  ┌────────┐  │       └──────┼▶ Ihp web service│ ││
│ │  │Postgres│  ◀──────────────┼▶ ConyMony blog  │ ││
│ │  └────────┘  │              │└────────────────┘ ││
│ └──────────────┘              └───────────────────┘│
└────────────────────────────────────────────────────┘
```

# TODO

- [x] figure out how to separate production-manjaroo and development-ubuntu
- [ ] create playbook to install QEMU
- [ ] figure out how to spinup vm to test ansible (QEMU)
- [ ] create playbook to install docker
  - [ ] set up playbook so that prod and dev docker installation differs

