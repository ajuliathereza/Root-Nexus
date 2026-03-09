# Hardware & Benchmarks — PC Atual (Baseline)

Autor: Júlia Thereza
Data: 2026-03-09
Objetivo: Documentar o hardware atual do meu notebook e registrar benchmarks como linha de base para futuras comparações, análises de desempenho e possíveis upgrades.

Tags: #hardware #benchmark #linux #windows #devops #infra

> **Autor:** Júlia Thereza  
> **Data:** 2026-02-21  
> **Objetivo:** Documentar hardware atual e registrar benchmarks para comparação futura.

**Tags:** #hardware #benchmark #linux #windows #devops #infra

---

## 1) Visão geral do sistema

### 1.1 Ambiente

- **Modelo do equipamento:** Dell Inspiron 5468
    
- **Tipo:** Notebook
    
- **Configuração:** Multi-Boot
    
- **Linux:** Ubuntu 24.04.4 LTS (Noble Numbat)
    
- **Windows:** Windows 11
    
- **Kali Linux**: Kali 2025.4 - 12th December, 2025 - Kernel 6.16.0, Xfce 4.20.5.
### 1.2 Kernel, firmware e arquitetura

- **Kernel Linux:** `6.17.0-14-generic`
    
- **Arquitetura:** `x86_64`
    
- **Firmware / BIOS:** Dell Inc. `1.18.0`
    
- **Data da BIOS:** `2022-01-11`
    
- **Modo de boot:** UEFI
    

### 1.3 Resumo rápido

- **CPU:** Intel Core i3-6006U @ 2.00GHz
    
- **Cores / Threads:** 2 / 4
    
- **GPU:** Intel HD Graphics 520
    
- **RAM:** 12 GB DDR4
    
- **Armazenamento:** SSD SATA Kingston A400 480 GB
    
- **Particionamento:** GPT
    
- **Virtualização:** VT-x disponível
    
- **Rede sem fio:** Qualcomm Atheros QCA9565 / AR9565
    
- **Rede cabeada:** Realtek RTL810xE Fast Ethernet
---

## 2) Inventário de hardware

### 2.1 Processador (CPU)

- **Modelo:** Intel(R) Core(TM) i3-6006U CPU @ 2.00GHz
    
- **Arquitetura:** x86_64
    
- **Modos operacionais:** 32-bit e 64-bit
    
- **Cores / Threads:** 2 cores / 4 threads
    
- **Threads por núcleo:** 2
    
- **Soquetes:** 1
    
- **Frequência mínima:** 400 MHz
    
- **Frequência máxima:** 2000 MHz
    
- **Virtualização:** VT-x
    
- **NUMA:** 1 nó
    

#### Cache

- **L1d:** 64 KiB (2 instâncias)
    
- **L1i:** 64 KiB (2 instâncias)
    
- **L2:** 512 KiB (2 instâncias)
    
- **L3:** 3 MiB
    

#### Análise

O Intel Core i3-6006U é um processador de entrada da 6ª geração da Intel, voltado para tarefas cotidianas, estudo, produtividade, navegação, documentação técnica, terminal e desenvolvimento leve.  
Ele atende bem a cargas moderadas, mas tem limitações em atividades mais pesadas, como múltiplas máquinas virtuais, compilação intensa, renderização, edição de vídeo e multitarefa muito agressiva.

Também há mitigação para diversas vulnerabilidades conhecidas, o que é relevante em contexto de segurança e estabilidade do sistema.
#### Saída do `lscpu` (raw)


```txt 
moonlher@moonlher:~$ lscpu
Arquitetura:                  x86_64
  Modo(s) operacional da CPU: 32-bit, 64-bit
  Tamanhos de endereço:       39 bits physical, 48 bits vi
                              rtual
  Ordem dos bytes:            Little Endian
CPU(s):                       4
  Lista de CPU(s) on-line:    0-3
ID de fornecedor:             GenuineIntel
  Nome do modelo:             Intel(R) Core(TM) i3-6006U C
                              PU @ 2.00GHz
    Família da CPU:           6
    Modelo:                   78
    Thread(s) per núcleo:     2
    Núcleo(s) por soquete:    2
    Soquete(s):               1
    Step:                     3
    CPU(s) MHz de escala:     85%
    CPU MHz máx.:             2000,0000
    CPU MHz mín.:             400,0000
    BogoMIPS:                 3999,93
    Opções:                   fpu vme de pse tsc msr pae m
                              ce cx8 apic sep mtrr pge mca
                               cmov pat pse36 clflush dts 
                              acpi mmx fxsr sse sse2 ss ht
                               tm pbe syscall nx pdpe1gb r
                              dtscp lm constant_tsc art ar
                              ch_perfmon pebs bts rep_good
                               nopl xtopology nonstop_tsc 
                              cpuid aperfmperf pni pclmulq
                              dq dtes64 monitor ds_cpl vmx
                               est tm2 ssse3 sdbg fma cx16
                               xtpr pdcm pcid sse4_1 sse4_
                              2 x2apic movbe popcnt tsc_de
                              adline_timer aes xsave avx f
                              16c rdrand lahf_lm abm 3dnow
                              prefetch cpuid_fault epb pti
                               ssbd ibrs ibpb stibp tpr_sh
                              adow flexpriority ept vpid e
                              pt_ad fsgsbase tsc_adjust sg
                              x bmi1 avx2 smep bmi2 erms i
                              nvpcid mpx rdseed adx smap c
                              lflushopt intel_pt xsaveopt 
                              xsavec xgetbv1 xsaves dtherm
                               arat pln pts hwp hwp_notify
                               hwp_act_window hwp_epp vnmi
                               md_clear flush_l1d arch_cap
                              abilities
Recursos de virtualização:    
  Virtualização:              VT-x
Caches (soma de todos):       
  L1d:                        64 KiB (2 instâncias)
  L1i:                        64 KiB (2 instâncias)
  L2:                         512 KiB (2 instâncias)
  L3:                         3 MiB (1 instância)
NUMA:                         
  Nó(s) de NUMA:              1
  CPU(s) de nó0 NUMA:         0-3
Vulnerabilidades:             
  Gather data sampling:       Vulnerable: No microcode
  Ghostwrite:                 Not affected
  Indirect target selection:  Not affected
  Itlb multihit:              KVM: Mitigation: Split huge 
                              pages
  L1tf:                       Mitigation; PTE Inversion; V
                              MX conditional cache flushes
                              , SMT vulnerable
  Mds:                        Mitigation; Clear CPU buffer
                              s; SMT vulnerable
  Meltdown:                   Mitigation; PTI
  Mmio stale data:            Mitigation; Clear CPU buffer
                              s; SMT vulnerable
  Old microcode:              Not affected
  Reg file data sampling:     Not affected
  Retbleed:                   Mitigation; IBRS
  Spec rstack overflow:       Not affected
  Spec store bypass:          Mitigation; Speculative Stor
                              e Bypass disabled via prctl
  Spectre v1:                 Mitigation; usercopy/swapgs 
                              barriers and __user pointer 
                              sanitization
  Spectre v2:                 Mitigation; IBRS; IBPB condi
                              tional; STIBP conditional; R
                              SB filling; PBRSB-eIBRS Not 
                              affected; BHI Not affected
  Srbds:                      Mitigation; Microcode
  Tsa:                        Not affected
  Tsx async abort:            Not affected
  Vmscape:                    Mitigation; IBPB before exit
                               to userspace
```

### 2.2 Memória RAM

- **Capacidade total instalada:** 12 GiB
    
- **Capacidade máxima suportada pela placa:** 16 GB
    
- **Slots físicos:** 2
    
- **Slots ocupados:** 2
    
- **Tipo:** DDR4 SODIMM
    
- **Correção de erro:** Não possui
    

#### Módulo 1

- **Capacidade:** 8 GB
    
- **Fabricante:** Samsung
    
- **Part Number:** `M471A1K43DB1-CTD`
    
- **Velocidade nominal:** 2667 MT/s
    
- **Velocidade configurada:** 2133 MT/s
    
- **Tensão:** 1.2 V
    

#### Módulo 2

- **Capacidade:** 4 GB
    
- **Fabricante:** Hitachi
    
- **Part Number:** `TMA851S6AFR6N-UHSC`
    
- **Velocidade nominal:** 2400 MT/s
    
- **Velocidade configurada:** 2133 MT/s
    
- **Tensão:** 1.2 V
    

#### Uso no momento da coleta

- **RAM usada:** 5,7 GiB
    
- **RAM livre:** 1,8 GiB
    
- **Buff/cache:** 5,2 GiB
    
- **Disponível:** 5,7 GiB
    
- **Swap:** 4,0 GiB
    
- **Uso de swap no momento da coleta:** 0 B
    

#### Análise

O sistema possui **12 GB de RAM**, o que ainda é uma quantidade razoável para estudo, multitarefa moderada, navegação com várias abas, terminal, containers leves e uso geral de desktop.

Há, porém, uma configuração mista de memória:

- um módulo de **8 GB**
    
- um módulo de **4 GB**
    
- velocidades nominais diferentes (**2667 MT/s** e **2400 MT/s**)
    

Ambos estão operando em **2133 MT/s**, o que indica ajuste para compatibilidade do sistema. Isso não chega a ser um problema grave, mas mostra que a memória não está operando no maior clock nominal dos módulos. Para upgrade futuro, uma configuração **2x8 GB DDR4 igualada** seria mais limpa e equilibrada.




### 2.3 Placa-mãe e firmware

- **Fabricante do sistema:** Dell Inc.
    
- **Modelo do notebook:** Inspiron 5468
    
- **SKU:** 07AC
    
- **Família:** Inspiron
    

#### Placa-mãe

- **Fabricante:** Dell Inc.
    
- **Modelo:** `0KCKCP`
    
- **Versão:** `A01`
    

#### BIOS / Firmware

- **Vendor:** Dell Inc.
    
- **Versão:** `1.18.0`
    
- **Release Date:** `01/11/2022`
    
- **ROM Size:** 16 MB
    
- **Recursos relevantes:** UEFI, ACPI, USB boot, smart battery, network boot
    

#### Análise

O equipamento utiliza firmware Dell relativamente recente para a plataforma, com suporte a **UEFI**, o que é coerente com a estrutura de dual-boot identificada no disco.  
A documentação de firmware e placa-mãe é importante para manutenção, atualização de BIOS e avaliação de compatibilidade de upgrades.


### 2.4 GPU e drivers

- **GPU:** Intel Corporation Skylake GT2 [HD Graphics 520]
    
- **Modelo comercial:** Intel HD Graphics 520
    
- **Tipo:** iGPU (integrada ao processador)
    
- **Barramento:** PCIe / onboard
    
- **Driver em uso no kernel:** `i915`
    
- **Framebuffer detectado:** `/dev/fb0`
    
- **Resolução detectada:** `1366x768`
    

#### Identificação

- **PCI ID:** `00:02.0`
    
- **Subsystem:** Dell Skylake GT2 [HD Graphics 520]
    
- **DeviceName:** Onboard IGD
    

#### Análise

A Intel HD Graphics 520 é uma GPU integrada voltada para uso cotidiano.  
Ela é suficiente para:

- interface gráfica do sistema
    
- navegação web
    
- reprodução de vídeos
    
- estudo
    
- programação
    
- tarefas leves de produtividade
    

Por outro lado, ela não é uma solução adequada para:

- jogos modernos exigentes
    
- renderização 3D pesada
    
- workloads gráficos avançados
    
- edição de vídeo mais intensa
    

Como é uma **iGPU**, ela depende da memória RAM do sistema, então o desempenho gráfico também é afetado pela configuração da memória instalada.

#### Observação

O comando `glxinfo` ainda não foi executado porque o pacote `mesa-utils` não estava instalado no momento da coleta.  
Assim, ainda faltam:

- renderizador OpenGL
    
- vendor OpenGL
    
- versão OpenGL
#### Saída do `lspci` (raw)
```txt
00:02.0 VGA compatible controller: Intel Corporation Skylake GT2 [HD Graphics 520] (rev 07)
  
```



### 2.5 Armazenamento

- **Disco principal:** Kingston SA400S37480G
    
- **Capacidade bruta:** 480.103.981.056 bytes (480 GB)
    
- **Capacidade utilizável reportada:** 447,13 GiB
    
- **Tipo:** SSD SATA
    
- **Interface SATA:** SATA 3.2, 6.0 Gb/s
    
- **TRIM:** disponível
    
- **Tabela de partição:** GPT
    

#### Partições

- **/dev/sda1** — 512 MiB — FAT32 — EFI System Partition — montada em `/boot/efi`
    
- **/dev/sda2** — 117,2 GiB — NTFS — partição Windows
    
- **/dev/sda3** — 97,7 GiB — ext4 — montada em `/`
    
- **/dev/sda4** — 58,6 GiB — ext4 — não montada no momento da coleta
    
- **/dev/sda5** — 173,2 GiB — NTFS — label `DataVault`
    

#### Espaço em uso

- **Partição raiz `/dev/sda3`:** 96G total
    
- **Usado:** 54G
    
- **Livre:** 38G
    
- **Uso:** 59%
    

#### Análise

A máquina utiliza um SSD SATA Kingston A400 de 480 GB com particionamento GPT e estrutura típica de dual-boot em UEFI.  
A divisão do armazenamento mostra separação entre:

- partição EFI
    
- sistema Linux
    
- partições Windows / dados
    
- uma partição ext4 extra não montada no momento da coleta
    

A ocupação atual da partição raiz está em **59%**, o que ainda é aceitável. O SSD está com espaço suficiente para uso normal do sistema.


### 2.6 Saúde do SSD (SMART)

- **Modelo:** KINGSTON SA400S37480G
    
- **Firmware:** `SBFKQ1.3`
    
- **SMART:** suportado e habilitado
    
- **Resultado geral de saúde:** **PASSED**
    
- **Horas de uso:** 2764
    
- **Ciclos de energia:** 1107
    
- **Temperatura atual:** 30°C
    
- **Temperatura mínima / máxima registrada:** 13°C / 50°C
    
- **Vida útil restante do SSD:** **95**
    
- **TRIM:** disponível
    

#### Outros indicadores

- **Unsafe Shutdown Count:** 156
    
- **Reallocated Event Count:** 0
    
- **Reported Uncorrect:** 0
    
- **Program Fail Count:** 0
    
- **Erase Fail Count:** 0
    

#### Observação importante

O atributo:

- **SATA_CRC_Error_Count: 851998**
    

está muito alto. Isso merece atenção. Em muitos casos, esse tipo de contador elevado pode estar relacionado a problema histórico de comunicação SATA, mau contato, cabo/conector ou alguma instabilidade de interface — e não necessariamente desgaste interno do SSD em si.  
Como se trata de notebook, vale apenas registrar isso no relatório como um ponto de observação técnica.

#### Análise

Apesar desse contador chamar atenção, o estado geral do SSD está positivo:

- saúde geral aprovada
    
- vida útil restante em 95
    
- sem falhas críticas de leitura/escrita
    
- sem realocação relevante
    
- temperatura normal
    

Ou seja, **o SSD aparenta estar funcional e em bom estado geral**, mas com um indicador de comunicação SATA que vale monitorar.

---

2.6 Saúde do SSD (SMART)

Modelo: KINGSTON SA400S37480G

Firmware: SBFKQ1.3

SMART: suportado e habilitado

Resultado geral de saúde: PASSED

Horas de uso: 2764

Ciclos de energia: 1107

Temperatura atual: 30°C

Temperatura mínima / máxima registrada: 13°C / 50°C

Vida útil restante do SSD: 95

TRIM: disponível

Outros indicadores

Unsafe Shutdown Count: 156

Reallocated Event Count: 0

Reported Uncorrect: 0

Program Fail Count: 0

Erase Fail Count: 0

Observação importante

O atributo:

SATA_CRC_Error_Count: 851998

está muito alto. Isso merece atenção. Em muitos casos, esse tipo de contador elevado pode estar relacionado a problema histórico de comunicação SATA, mau contato, cabo/conector ou alguma instabilidade de interface — e não necessariamente desgaste interno do SSD em si.
Como se trata de notebook, vale apenas registrar isso no relatório como um ponto de observação técnica.

Análise

Apesar desse contador chamar atenção, o estado geral do SSD está positivo:

saúde geral aprovada

vida útil restante em 95

sem falhas críticas de leitura/escrita

sem realocação relevante

temperatura normal

Ou seja, o SSD aparenta estar funcional e em bom estado geral, mas com um indicador de comunicação SATA que vale monitorar.


### 2.8 Bateria e energia

- **Bateria detectada:** BAT0
    
- **Fabricante:** Panasonic
    
- **Modelo:** DELL 78V9D94
    
- **Tecnologia:** Lithium-ion
    
- **Estado no momento da coleta:** fully-charged
    
- **Carga:** 100%
    
- **Energia atual:** 35,3868 Wh
    
- **Capacidade cheia atual:** 35,3868 Wh
    
- **Capacidade de fábrica (design):** 41,44 Wh
    
- **Capacidade remanescente:** **85,3929%**
    
- **Tensão:** 16,572 V
    

#### Análise

A bateria ainda mantém cerca de **85,39% da capacidade original**, o que é um resultado bom para um notebook dessa geração.  
Isso indica desgaste natural, mas ainda com condição utilizável para mobilidade. Não parece ser uma bateria em estado crítico.


### 2.9 Sensores e temperaturas

#### Leituras no momento da coleta

- **CPU:** 42°C
    
- **Package CPU:** 43°C
    
- **Core 0:** 42°C
    
- **Core 1:** 43°C
    
- **Chipset / PCH:** 40°C
    
- **Temperatura ambiente reportada:** 31°C
    
- **SODIMM:** 35°C
    

#### Ventoinha

- **Processor Fan:** 0 RPM no momento da leitura  
    (mínimo 0 RPM / máximo 4900 RPM)
    

#### Análise

As temperaturas registradas estão **boas para estado de repouso ou carga leve**:

- CPU entre 42–43°C
    
- chipset em 40°C
    
- memória em 35°C
    

Não há sinal evidente de aquecimento anormal nessa coleta.  
O sistema parece operar dentro de uma faixa térmica saudável em uso leve.


## 3) Benchmarks

### 3.1 CPU — Sysbench

`sysbench cpu --cpu-max-prime=20000 run`

**Resultado**

- **Events per second:** 270.60
    
- **Tempo total:** 10.0011 s
    
- **Total de eventos:** 2707
    
- **Latência mínima:** 3.66 ms
    
- **Latência média:** 3.69 ms
    
- **Latência máxima:** 4.70 ms
    
- **95th percentile:** 3.75 ms
    

#### Análise

O resultado é coerente com um processador dual-core / quad-thread de entrada, focado em eficiência e tarefas leves.  
Esse benchmark serve bem como linha de base para futuras comparações após manutenção, troca de pasta térmica, upgrade ou mudança de sistema.


3.2 Disco — `hdparm`

`sudo hdparm -Tt /dev/sda `

**Resultado**

- **Timing cached reads:** 5943.86 MB/s
    
- **Timing buffered disk reads:** 336.09 MB/s
    

#### Análise

O valor relevante aqui é o de leitura do disco:

- **336 MB/s** está dentro de um patamar coerente para SSD SATA de entrada
    

O valor de cached reads representa leitura em cache/memória e não deve ser interpretado como velocidade real do SSD.

3.3 Disco — `dd`

`dd if=/dev/zero of=teste.bin bs=1G count=1 oflag=direct `

**Resultado**

- **Escrita sequencial:** 366 MB/s
    

#### Análise

A taxa de escrita observada também está coerente com um SSD SATA de entrada e combina com o perfil do Kingston A400.  
Para o uso cotidiano do sistema, esse desempenho é mais do que suficiente para boot, abertura de programas e responsividade geral.

### 3.4 GPU — Benchmark gráfico

O `glmark2-x11` foi instalado, mas o resultado do benchmark ainda não foi registrado nesta coleta.

#### Pendente

Executar:

`glmark2 `

### 3.5 OpenGL / renderizador gráfico

Também ficou pendente a coleta do renderizador OpenGL.

#### Pendente

Instalar:
`sudo apt install mesa-utils `

Executar:
`glxinfo | grep -E "OpenGL vendor|OpenGL renderer|OpenGL version`


## 4) Análise geral do equipamento

### 4.1 Perfil da máquina

Este notebook se posiciona como uma máquina adequada para:

- estudos
    
- programação leve
    
- documentação técnica
    
- navegação
    
- uso de terminal
    
- automação
    
- containers leves
    
- produtividade geral
    
- uso diário em Linux e Windows
    

### 4.2 Pontos fortes

- SSD SATA com desempenho satisfatório
    
- 12 GB de RAM ainda utilizáveis para multitarefa moderada
    
- dual-boot funcional
    
- bateria ainda com boa capacidade
    
- temperaturas saudáveis em uso leve
    
- hardware estável para produtividade e estudo
    

### 4.3 Limitações

- CPU já é antiga e limitada para cargas pesadas
    
- GPU integrada básica
    
- RAM em configuração mista
    
- Ethernet limitada a 100 Mbit/s
    
- há um contador SMART de erro CRC SATA extremamente alto, que deve ser monitorado
    

### 4.4 Gargalos mais prováveis

Os principais limitadores do sistema, hoje, são:

1. **CPU**
    
2. **GPU integrada**
    
3. **Configuração de RAM mista**
    
4. **Possível histórico de erro de comunicação SATA**
    

### 4.5 Estado atual

No geral, o notebook está em **estado funcional e saudável para seu perfil de uso**, principalmente em tarefas leves e moderadas.  
Ele continua sendo uma máquina útil para estudo, documentação, Linux, terminal e atividades técnicas não muito pesadas.

## 5) Próximos passos para completar o baseline

Ainda faltam dois itens para fechar a documentação com mais força:

### 5.1 OpenGL / stack gráfica

` sudo apt install mesa-utils
`glxinfo | grep -E "OpenGL vendor|OpenGL renderer|OpenGL version

### 5.2 Benchmark gráfico  

`glmark2


## 6) Conclusão

O Dell Inspiron 5468 documentado nesta linha de base apresenta uma configuração equilibrada para uso cotidiano, estudo, produtividade e desenvolvimento leve. O sistema combina um processador Intel Core i3-6006U, 12 GB de RAM DDR4 em configuração mista, SSD SATA Kingston de 480 GB, GPU integrada Intel HD Graphics 520 e Multi-boot com Ubuntu 24.04.4 LTS, Windows 11 e Kali Linux.

Os testes mostram que o equipamento continua funcional e responsivo para o perfil de uso proposto, com temperaturas saudáveis, bateria ainda em bom estado e SSD com desempenho coerente para a categoria. O principal ponto de atenção está no histórico de erros CRC SATA reportado pelo SMART, que merece monitoramento.

Como baseline técnico, este documento estabelece uma referência confiável para futuras comparações após upgrades, manutenção, ajustes de sistema ou novos benchmarks.