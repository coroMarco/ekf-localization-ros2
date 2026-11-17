# EKF Localization ROS 2

Stima di stato (posizione e orientamento) con un Extended Kalman Filter in C++ e ROS 2, che fonde IMU e odometria, gestendo sensori in ritardo o temporaneamente persi.

> **Stato:** in fase di avvio.

## Obiettivi

- Implementare un EKF da zero in C++ (Eigen).
- Fondere IMU e odometria per stimare posizione e orientamento.
- Gestire misure in ritardo e sensori persi.
- Valutare l'errore rispetto al ground truth.
- Usare `robot_localization` solo come riferimento di confronto finale.

## Dati

- **Primario:** EuRoC MAV (IMU e ground truth). Il dataset non è versionato in questa repo e va messo in `data/`.
- **Alternativo:** un bag ROS 2 di un robot simulato.

## Strumenti

- C++17, ROS 2, Eigen, `colcon`
- Python solo per l'analisi dei risultati

## Struttura
ekf-localization-ros2/
├── README.md
├── .gitignore
├── src/
│ └── ekf_estimator/ # package ROS 2 (da creare)
├── data/ # dataset locali, non versionati
├── scripts/ # analisi: RMSE, grafici
└── docs/
└── limitations.md # limiti e assunzioni


## Deliverable

- [ ] Filtro EKF IMU + odometria funzionante in C++/ROS 2
- [ ] Gestione di misure in ritardo e sensori persi
- [ ] Grafico dell'errore rispetto al ground truth
- [ ] Tabella RMSE in posizione e orientamento
- [ ] Confronto di riferimento con `robot_localization`
- [ ] Sezione dei limiti

## Limiti

Da completare durante il progetto.
EOF