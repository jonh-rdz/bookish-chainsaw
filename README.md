# bookish-chainsaw

graph LR
    A[CSV File] -->|Extract| B(Pandas / Python)
    B -->|Transform| C{Reglas de Negocio}
    C -->|Load / JSON| D[(Supabase / PostgreSQL)]
    D -->|Analítica SQL| E[Detección de Anomalías]
    F[Apache Airflow] -.->|Orquesta diariamente| B
    F -.->|Orquesta| E
