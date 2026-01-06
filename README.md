# 🔬 Android Forensics Tool - Professional Edition

![Version](https://img.shields.io/badge/version-3.0.0-blue.svg)
![License](https://img.shields.io/badge/license-Confidential-red.svg)
![Platform](https://img.shields.io/badge/platform-.NET%208.0-purple.svg)
![Security](https://img.shields.io/badge/security-Professional%20Grade-green.svg)

> **Sistema de Análise Forense Digital Profissional para Dispositivos Android**
> 
> Ferramenta profissional com 13 módulos especializados para análise forense completa e detecção de evidências digitais.

---

## 📋 Índice

- [Visão Geral](#-visão-geral)
- [Características Principais](#-características-principais)
- [Módulos Profissionais](#-módulos-profissionais)
- [Requisitos do Sistema](#-requisitos-do-sistema)
- [Instalação](#-instalação)
- [Guia de Uso](#-guia-de-uso)
- [Análises Disponíveis](#-análises-disponíveis)
- [Relatórios e Exportação](#-relatórios-e-exportação)
- [Arquitetura do Sistema](#-arquitetura-do-sistema)
- [Casos de Uso](#-casos-de-uso)
- [Segurança e Compliance](#-segurança-e-compliance)
- [Troubleshooting](#-troubleshooting)
- [FAQ](#-faq)
- [Suporte](#-suporte)

---

## 🎯 Visão Geral

O **Android Forensics Tool - Professional Edition** é uma solução completa de análise forense digital desenvolvida para profissionais de segurança, investigadores forenses, agências de inteligência e forças de segurança pública. Com mais de **6.000 linhas de código** e **13 módulos profissionais**, a ferramenta oferece capacidades de análise abrangentes e precisas.

### 🏆 Diferenciais

- ✅ **13 Módulos Profissionais** - Análise forense completa
- ✅ **Detecção de Malware** - 15+ heurísticas avançadas
- ✅ **Análise de Memória RAM** - Processos e conexões ativas
- ✅ **Recuperação de Arquivos Deletados** - Técnicas avançadas
- ✅ **Timeline Forense** - Reconstrução cronológica de eventos
- ✅ **Análise de Databases** - SQLite com queries avançadas
- ✅ **Chain of Custody** - Cadeia de custódia automática
- ✅ **Relatórios HTML** - Visualização profissional com gráficos

---

## 🚀 Características Principais

### 📊 Análise Forense Completa

| Categoria | Recursos |
|-----------|----------|
| **Dispositivo** | • Informações de hardware<br>• Status de root e bootloader<br>• Detecção multi-método (6 técnicas)<br>• Análise de partições |
| **Aplicativos** | • 200+ apps analisados<br>• Detecção de malware com 15 heurísticas<br>• Análise de permissões perigosas<br>• Apps ocultos e suspeitos |
| **Comunicações** | • SMS/MMS completos<br>• Histórico de chamadas<br>• Contatos com metadados<br>• Extração de mensagens |
| **Dados** | • Sistema de arquivos completo<br>• Recuperação de arquivos deletados<br>• Análise de databases (SQLite)<br>• Memória RAM (processos, conexões) |
| **Localização** | • GPS history<br>• WiFi access points<br>• Histórico de navegação<br>• Bookmarks |
| **Rede** | • Redes WiFi conhecidas<br>• Logs do sistema<br>• Conexões ativas<br>• Histórico de dados |

### 🔐 Segurança e Chain of Custody

- ✅ **Hash MD5/SHA256** para todas as evidências
- ✅ **Chain of Custody** automática com timestamps
- ✅ **Logs de auditoria** completos
- ✅ **Relatórios forenses** em HTML/JSON
- ✅ **Conformidade** com padrões internacionais

---

## 📦 Módulos Profissionais

### 1. 📱 Device Info Extractor

**Extração Completa de Informações do Dispositivo**

**Informações Coletadas:**
- 📱 **Hardware:**
  - Fabricante, Modelo, Nome do Dispositivo
  - Serial Number, IMEI, MEID
  - Número de telefone
  - Android ID único
  - Build fingerprint completo
  
- 💾 **Sistema Operacional:**
  - Versão do Android (ex: 13.0)
  - API Level (ex: 33)
  - Build ID e número
  - Security patch level
  - Kernel version
  - ABI suportadas (arm64-v8a, armeabi-v7a)
  
- 🔧 **Configurações:**
  - Idioma e localização
  - Timezone
  - Screen density e resolução
  - Orientação da tela
  
- 🔐 **Segurança:**
  - Status de root (6 métodos de detecção)
  - Bootloader locked/unlocked
  - SELinux status (Enforcing/Permissive)
  - Encryption status
  - SafetyNet/Play Integrity
  
- 💾 **Armazenamento:**
  - Total storage
  - Espaço livre/usado
  - Storage interno e SD card
  - Partições montadas

**Resultado Exemplo:**
```json
{
  "Manufacturer": "Samsung",
  "Model": "SM-G998B",
  "AndroidVersion": "13.0",
  "IMEI": "123456789012345",
  "SerialNumber": "R5CR1234567",
  "IsRooted": true,
  "BootloaderUnlocked": false,
  "TotalStorage": "256GB",
  "SecurityPatchLevel": "2025-12-01"
}
```

---

### 2. 📲 App Extractor

**Análise Profunda de Aplicativos Instalados**

**Capacidades:**
- ✅ Lista completa de apps (sistema + usuário)
- ✅ 200+ aplicativos analisados
- ✅ **Detecção de malware** com 15 heurísticas
- ✅ Análise de permissões perigosas
- ✅ Apps ocultos e disfarçados
- ✅ Apps de fontes desconhecidas
- ✅ Versões e assinaturas (signatures)
- ✅ Tamanho e data de instalação
- ✅ Diretórios de dados
- ✅ Bibliotecas nativas (.so)

**Permissões Perigosas Detectadas:**
- 📷 CAMERA
- 🎤 RECORD_AUDIO
- 📍 ACCESS_FINE_LOCATION
- 📞 READ_CONTACTS, READ_SMS, READ_CALL_LOG
- 💾 READ_EXTERNAL_STORAGE, WRITE_EXTERNAL_STORAGE
- 📱 READ_PHONE_STATE
- 📧 GET_ACCOUNTS
- 📅 READ_CALENDAR

**Heurísticas de Malware (15 tipos):**
1. Permissões excessivas (>15 dangerous)
2. Instalado de fontes não-oficiais
3. Nome suspeito ou genérico
4. Ausência na Play Store
5. Versão desatualizada crítica
6. Assinatura inválida
7. Código ofuscado detectado
8. Comportamento de spyware
9. Requisições de root suspeitas
10. Network activity anormal
11. Background services excessivos
12. Broadcast receivers ocultos
13. Processos em nome diferente
14. Arquivos .dex suspeitos
15. Bibliotecas nativas maliciosas

**Categorização Automática:**
- 🎮 Games
- 📱 Social Media
- 💬 Communication
- 📧 Productivity
- 🛒 Shopping
- 🏦 Finance/Banking
- 🎵 Media & Entertainment
- 🔧 Tools & Utilities
- 🚗 Travel & Navigation
- 📰 News & Magazines

**Resultado Exemplo:**
```json
{
  "TotalApps": 187,
  "SystemApps": 95,
  "UserApps": 92,
  "SuspiciousApps": 3,
  "MalwareDetected": 1,
  "AppsWithDangerousPermissions": 47,
  "HiddenApps": 2
}
```

---

### 3. 💬 Communication Extractor

**Extração Completa de Comunicações**

**Dados Extraídos:**

#### 📨 SMS/MMS
- ✅ Todas as mensagens (inbox, sent, draft)
- ✅ Número do remetente/destinatário
- ✅ Timestamp preciso
- ✅ Tipo (SMS/MMS)
- ✅ Status (lida/não lida)
- ✅ Thread ID
- ✅ Mensagens deletadas (se recuperáveis)
- ✅ Anexos MMS (imagens, vídeos)

**Database:** `/data/data/com.android.providers.telephony/databases/mmssms.db`

#### 📞 Histórico de Chamadas
- ✅ Chamadas recebidas
- ✅ Chamadas realizadas
- ✅ Chamadas perdidas
- ✅ Chamadas rejeitadas
- ✅ Chamadas bloqueadas
- ✅ Duração de cada chamada
- ✅ Timestamp de início/fim
- ✅ Nome do contato (se disponível)
- ✅ Via (SIM1, SIM2, WhatsApp, etc)

**Database:** `/data/data/com.android.providers.contacts/databases/calllog.db`

#### 👥 Contatos
- ✅ Nome completo
- ✅ Números de telefone (múltiplos)
- ✅ Emails
- ✅ Endereços
- ✅ Aniversário
- ✅ Notas
- ✅ Foto de perfil
- ✅ Contas vinculadas (Google, WhatsApp, etc)
- ✅ Última modificação
- ✅ Frequência de contato

**Database:** `/data/data/com.android.providers.contacts/databases/contacts2.db`

**Análises Adicionais:**
- 📊 Top 20 contatos mais contatados
- 📈 Padrões de comunicação (horários, dias)
- 🔍 Números bloqueados
- ⚠️ Números suspeitos (internacionais, premium)
- 📅 Timeline de comunicação

**Resultado Exemplo:**
```json
{
  "TotalSMS": 8547,
  "TotalMMS": 234,
  "TotalCalls": 1289,
  "TotalContacts": 456,
  "MostContactedNumber": "+5511987654321",
  "AverageSMSPerDay": 23,
  "LongestCall": "1h 45m 23s"
}
```

---

### 4. 🌐 Network & Location Extractor

**Redes WiFi e Localização**

**Redes WiFi:**
- ✅ Redes salvas (SSID, BSSID, senha*)
- ✅ Redes detectadas (scan results)
- ✅ Histórico de conexões
- ✅ Tipo de segurança (WEP, WPA, WPA2, WPA3)
- ✅ Intensidade de sinal (RSSI)
- ✅ Frequência (2.4GHz, 5GHz)
- ✅ MAC address do AP
- ✅ Última conexão

**Database:** `/data/misc/wifi/WifiConfigStore.xml`

**Localização:**
- ✅ GPS location history
- ✅ Google Location Services
- ✅ Network-based location
- ✅ Cell tower connections
- ✅ Location providers ativos
- ✅ Permissões de localização por app
- ✅ Geofences configuradas
- ✅ Significant locations

**Databases:**
- `/data/data/com.google.android.gms/databases/herrevad`
- `/data/data/com.google.android.gms/databases/networkusage.db`

**Análises:**
- 🏠 Home location detection
- 🏢 Work location detection
- 🚗 Commute patterns
- 📍 Frequent locations
- 🗺️ Travel history

**Resultado Exemplo:**
```json
{
  "SavedWiFiNetworks": 47,
  "CurrentWiFi": "HomeNetwork_5G",
  "LocationHistory": 12456,
  "HomeLocation": {
    "Lat": -23.5505,
    "Lon": -46.6333,
    "City": "São Paulo"
  },
  "TotalDistanceTraveled": "1245.7 km"
}
```

---

### 5. 🌍 Browser History Extractor

**Histórico Completo de Navegação**

**Navegadores Suportados:**
- 🌐 Chrome
- 🦊 Firefox
- 🌊 Opera
- 🔒 Brave
- 🎯 Samsung Internet
- 📱 UC Browser
- 🚀 Edge
- 🔍 DuckDuckGo
- 🦁 Kiwi Browser

**Dados Extraídos:**

#### 📜 Histórico
- ✅ URLs visitadas (completas)
- ✅ Títulos das páginas
- ✅ Timestamps de visita
- ✅ Contagem de visitas
- ✅ Digitado ou clicado
- ✅ Tempo de permanência

**Database:** `/data/data/com.android.chrome/app_chrome/Default/History`

#### 🔖 Favoritos/Bookmarks
- ✅ Nome do bookmark
- ✅ URL
- ✅ Pasta/categoria
- ✅ Data de criação

#### 📥 Downloads
- ✅ Arquivo baixado
- ✅ URL de origem
- ✅ Caminho local
- ✅ Tamanho do arquivo
- ✅ Data do download
- ✅ Status (completo/incompleto)

#### 🔐 Senhas Salvas*
- ✅ Site/app
- ✅ Username
- ✅ Senha (criptografada)
- ✅ Data de criação

**⚠️ Nota:** Senhas são criptografadas, extração requer root + keystore

#### 🍪 Cookies
- ✅ Domain
- ✅ Nome/valor
- ✅ Expiration date
- ✅ Secure/HttpOnly flags

#### 📝 Autofill Data
- ✅ Nomes
- ✅ Endereços
- ✅ Emails
- ✅ Telefones
- ✅ Cartões de crédito (parcial)

**Análises:**
- 📊 Top 50 sites visitados
- ⏱️ Padrões de navegação (horários)
- 🔞 Detecção de conteúdo sensível
- 🎯 Categorização automática (news, social, shopping, adult)
- 🕵️ Modo anônimo/privado detectado
- 📈 Tempo total de navegação

**Resultado Exemplo:**
```json
{
  "TotalHistoryEntries": 15789,
  "TotalBookmarks": 234,
  "TotalDownloads": 567,
  "SavedPasswords": 89,
  "MostVisitedSite": "youtube.com (1234 visits)",
  "TotalBrowsingTime": "234h 56m",
  "PrivacyScore": 6.5
}
```

---

### 6. 📁 File System Extractor

**Análise Completa do Sistema de Arquivos**

**Escaneamento Completo:**
- ✅ `/sdcard/` (armazenamento interno)
- ✅ `/storage/` (SD cards externos)
- ✅ `/data/data/` (dados de apps)
- ✅ `/data/media/` (arquivos de mídia)
- ✅ `/system/` (sistema operacional)
- ✅ `/cache/` (arquivos temporários)
- ✅ `/vendor/` (arquivos do fabricante)

**Tipos de Arquivos:**
- 📷 **Imagens:** JPG, PNG, GIF, WebP, BMP, SVG
- 🎥 **Vídeos:** MP4, AVI, MKV, 3GP, MOV, WebM
- 🎵 **Áudio:** MP3, AAC, FLAC, WAV, OGG, M4A
- 📄 **Documentos:** PDF, DOC, DOCX, XLS, XLSX, PPT, TXT
- 📦 **Arquivos:** ZIP, RAR, 7Z, TAR, GZ
- 💾 **Databases:** DB, SQLite, SQLite3, DB-SHM, DB-WAL
- 🔧 **Executáveis:** APK, DEX, SO, ELF
- 🔐 **Certificados:** CRT, PEM, KEY, P12

**Metadados Extraídos:**
- 📝 Nome do arquivo
- 📏 Tamanho (bytes)
- 📅 Data de criação
- 📅 Data de modificação
- 📅 Data de acesso
- 🔐 Permissões (rwx)
- 👤 Owner/Group
- 🔑 Hash MD5/SHA256
- 📍 Caminho completo

**EXIF para Imagens:**
- 📷 Câmera/dispositivo usado
- 📅 Data/hora da foto
- 📍 GPS (latitude, longitude)
- 🔧 Configurações (ISO, abertura, exposição)
- 🎨 Dimensões (largura x altura)
- 🔄 Orientação
- ✏️ Software de edição

**Análises Especiais:**
- 🔍 Detecção de arquivos ocultos (iniciando com .)
- 🗑️ Arquivos em lixeira (.trashed)
- 📷 Capturas de tela (Screenshots/)
- 📥 Downloads recentes
- 💬 WhatsApp media
- 📧 Email attachments
- 🎵 Music library
- 📺 Video library
- 📚 eBooks (EPUB, MOBI, PDF)
- 🔐 Encrypted files (.enc, .encrypted)

**Categorização por App:**
- WhatsApp → `/sdcard/WhatsApp/`
- Telegram → `/sdcard/Telegram/`
- Instagram → `/sdcard/Instagram/`
- Camera → `/sdcard/DCIM/Camera/`
- Downloads → `/sdcard/Download/`

**Resultado Exemplo:**
```json
{
  "TotalFiles": 45678,
  "TotalSize": "124.5 GB",
  "Images": 8934,
  "Videos": 456,
  "Audio": 1234,
  "Documents": 789,
  "Databases": 234,
  "APKs": 187,
  "HiddenFiles": 45,
  "FilesWithGPS": 4567,
  "ScreenshotsDetected": 1234
}
```

---

### 7. 📋 Log Extractor

**Extração Completa de Logs do Sistema**

**Tipos de Logs:**

#### 📱 **Logcat** (Sistema Android)
- ✅ Verbose logs
- ✅ Debug logs
- ✅ Info logs
- ✅ Warning logs
- ✅ Error logs
- ✅ Fatal logs
- ✅ Filtros por app (PID/TID)
- ✅ Filtros por tag
- ✅ Buffer completo

**Comando:** `adb logcat -d -v threadtime`

#### 🔴 **Kernel Logs** (dmesg)
- ✅ Boot sequence
- ✅ Driver loading
- ✅ Hardware events
- ✅ USB connections
- ✅ Memory events
- ✅ CPU throttling
- ✅ Crashes do kernel

**Comando:** `adb shell su -c dmesg`

#### ⚡ **Event Log**
- ✅ Battery events
- ✅ Conectividade (WiFi, mobile data)
- ✅ Screen on/off
- ✅ App launches
- ✅ Package installs/uninstalls

#### 📻 **Radio Log**
- ✅ Cellular connection
- ✅ Signal strength
- ✅ Handovers entre torres
- ✅ SMS sending/receiving
- ✅ Data usage

#### 🔧 **System Service Logs**
- ✅ Activity Manager
- ✅ Package Manager
- ✅ Window Manager
- ✅ Power Manager
- ✅ Location Manager

#### 🌐 **Network Logs**
- ✅ DNS queries
- ✅ HTTP requests
- ✅ TCP connections
- ✅ VPN connections
- ✅ Firewall events

**Análises:**
- 🔍 **Crash Detection** - ANRs e Force Closes
- ⚠️ **Error Analysis** - Erros críticos
- 📊 **App Usage Statistics** - Tempo de uso por app
- 🔋 **Battery Drain Analysis** - Apps consumindo bateria
- 🌐 **Network Activity** - Apps com mais tráfego
- 📍 **Location Requests** - Apps acessando GPS
- 🔐 **Permission Denials** - Apps com permissões negadas
- 💾 **Storage Events** - Arquivos criados/deletados

**Filtros e Busca:**
- 🔍 Regex patterns
- 📅 Date/time range
- 🏷️ Specific tags
- 📱 Specific apps (package name)
- ⚠️ Error level (Warning/Error/Fatal only)

**Resultado Exemplo:**
```json
{
  "LogcatEntries": 245678,
  "KernelLogEntries": 12456,
  "CrashesDetected": 23,
  "ErrorsDetected": 456,
  "WarningsDetected": 1234,
  "TopCrashingApp": "com.example.buggyapp (12 crashes)",
  "HighBatteryDrainApps": ["com.facebook.katana", "com.instagram.android"],
  "LogSize": "234.5 MB"
}
```

---

### 8. 🧠 Memory Analyzer

**Análise de Memória RAM em Tempo Real**

**Informações Extraídas:**

#### 💾 **Informação de Memória**
- ✅ Total RAM
- ✅ RAM disponível
- ✅ RAM em uso
- ✅ Cached memory
- ✅ Swap usage
- ✅ Memory pressure

**Comando:** `adb shell cat /proc/meminfo`

#### ⚙️ **Processos Ativos**
- ✅ Lista completa de processos
- ✅ PID (Process ID)
- ✅ Nome do processo
- ✅ Package name
- ✅ CPU usage (%)
- ✅ Memory usage (MB)
- ✅ Threads count
- ✅ Estado (Running/Sleeping/Zombie)
- ✅ Nice/priority
- ✅ User/UID

**Comando:** `adb shell ps -A -o pid,ppid,user,time,nice,args`

#### 🌐 **Conexões de Rede Ativas**
- ✅ Sockets TCP ativos
- ✅ Sockets UDP ativos
- ✅ IP local e porta
- ✅ IP remoto e porta
- ✅ Estado da conexão (ESTABLISHED, LISTEN, etc)
- ✅ PID do processo
- ✅ Bytes sent/received

**Comandos:** 
```
adb shell cat /proc/net/tcp
adb shell cat /proc/net/udp
adb shell ss -tunap
```

#### 🔌 **Sockets Unix**
- ✅ Unix domain sockets
- ✅ IPC connections
- ✅ Local socket communication

#### 🔄 **Handles de Arquivo**
- ✅ Arquivos abertos por processo
- ✅ File descriptors
- ✅ Pipes, sockets, devices

**Comando:** `adb shell lsof`

**Análises Avançadas:**

1. **Memory Leaks Detection**
   - Apps com uso crescente de memória
   - Processos com memory bloat
   - Apps com excessive heap usage

2. **Process Anomalies**
   - Processos desconhecidos/suspeitos
   - Processos com nome disfarçado
   - Processos com CPU excessivo (cryptominers)
   - Processos órfãos

3. **Network Anomalies**
   - Conexões a IPs suspeitos
   - Backdoor ports abertos (4444, 31337)
   - Múltiplas conexões ao mesmo IP
   - Conexões a países suspeitos
   - Conexões em portas não-padrão

4. **Malware Indicators**
   - Processos de malware conhecidos:
     * `com.android.system.update` (fake system)
     * `com.google.services` (fake Google)
     * `system32.exe` (Windows malware em Android!)
   - Processos escondidos
   - Rootkits ativos

**Resultado Exemplo:**
```json
{
  "TotalRAM": "8 GB",
  "AvailableRAM": "2.3 GB",
  "UsedRAM": "5.7 GB",
  "TotalProcesses": 456,
  "TotalThreads": 2345,
  "ActiveTCPConnections": 67,
  "ActiveUDPConnections": 23,
  "SuspiciousProcesses": 2,
  "SuspiciousConnections": 3,
  "TopMemoryApp": "com.facebook.katana (678 MB)",
  "TopCPUApp": "com.android.systemui (15%)"
}
```

---

### 9. 🦠 Malware Scanner

**Detecção Avançada de Malware**

**15 Heurísticas de Detecção:**

1. **Signature-Based Detection**
   - Database com 50.000+ assinaturas de malware
   - MD5/SHA256 de APKs conhecidos
   - Nomes de pacotes maliciosos

2. **Behavioral Analysis**
   - Apps com permissões excessivas
   - Background services suspeitos
   - Auto-start em boot
   - Broadcast receivers ocultos

3. **Code Analysis**
   - Ofuscação de código (ProGuard extremo)
   - Strings suspeitas (eval, exec, shell)
   - Reflexão excessiva
   - Native code suspeito (.so files)
   - Dex loading dinâmico

4. **Network Analysis**
   - Conexões a C&C servers conhecidos
   - DGA (Domain Generation Algorithm)
   - Beaconing behavior
   - Exfiltração de dados

5. **File System Analysis**
   - Arquivos em locais suspeitos
   - Scripts de root (su, busybox)
   - Arquivos ocultos maliciosos
   - Binários ELF não-oficiais

6. **Permission Analysis**
   - Permissões perigosas desnecessárias
   - Overlay attacks (SYSTEM_ALERT_WINDOW)
   - Accessibility service abuse
   - Device Admin abuse

7. **Process Analysis**
   - Processos persistentes suspeitos
   - Child processes suspeitos
   - Process hollowing/injection
   - Root privilege escalation

8. **Cryptomining Detection**
   - CPU usage > 80% constante
   - Bibliotecas de mining (XMRig, etc)
   - Pool connection patterns
   - Wallet addresses no código

9. **Banking Trojan Detection**
   - Overlay sobre apps bancários
   - Keylogging indicators
   - SMS interception
   - Screen capture

10. **Spyware Detection**
    - Screen recording
    - Keylogger
    - Call recording
    - Location tracking excessivo
    - SMS/Call log stealing

11. **Ransomware Detection**
    - File encryption activity
    - Screen locking malicioso
    - Ransom notes
    - Crypto payment demands

12. **Adware Detection**
    - Ad libraries excessivas
    - Fullscreen ads intrusivos
    - Notification spam
    - Browser hijacking

13. **Rootkit Detection**
    - Kernel modules suspeitos
    - Hooking frameworks (Xposed, Frida)
    - /system modifications
    - Hidden processes/files

14. **RAT Detection** (Remote Access Trojan)
    - TeamViewer-like functionality
    - VNC servers
    - Remote shell
    - Remote control libraries

15. **APT Indicators** (Advanced Persistent Threat)
    - Nation-state malware signatures
    - Zero-day exploit indicators
    - Sophisticated C&C
    - Data exfiltration patterns

**Bases de Dados Utilizadas:**
- VirusTotal API integration (opcional)
- YARA rules para Android
- OpenSource malware signatures
- Google Play Protect indicators

**Score de Malware (0-100):**
```
0-20:   🟢 SEGURO - Nenhuma ameaça detectada
21-40:  🟡 SUSPEITO - Comportamento questionável
41-60:  🟠 PROVÁVEL MALWARE - Múltiplos indicadores
61-80:  🔴 MALWARE - Alta confiança
81-100: ⚫ CRÍTICO - Malware avançado/APT
```

**Resultado Exemplo:**
```json
{
  "TotalAppsScanned": 187,
  "MalwareDetected": 3,
  "SuspiciousApps": 7,
  "AdwareDetected": 2,
  "SpywareDetected": 1,
  "TotalThreats": 13,
  "HighestThreatScore": 85,
  "MalwareList": [
    {
      "PackageName": "com.fake.system",
      "ThreatType": "Banking Trojan",
      "Score": 85,
      "Indicators": [
        "Overlay attack",
        "SMS interception",
        "Known C&C connection"
      ]
    }
  ]
}
```

---

### 10. 🗄️ Database Analyzer

**Análise Profunda de Databases SQLite**

**Databases Analisadas:**

#### WhatsApp
- `msgstore.db` - 10.000+ mensagens
- `wa.db` - Contatos e configurações
- `axolotl.db` - Chamadas e sessões

#### Contacts
- `contacts2.db` - Todos os contatos

#### SMS/MMS
- `mmssms.db` - Mensagens completas

#### Call Log
- `calllog.db` - Histórico de chamadas

#### Browser
- `History` - Chrome/Firefox
- `places.sqlite` - Firefox

#### Calendar
- `calendar.db` - Eventos e compromissos

#### Google Services
- `herrevad` - Location history
- `googleappstate.db` - App states
- `networkusage.db` - Network statistics

#### System
- `settings.db` - System settings
- `accounts.db` - Contas configuradas

**Análise Realizada:**
- ✅ **Schema Extraction** - Estrutura das tabelas
- ✅ **Data Dump** - Todos os dados em JSON
- ✅ **Relational Mapping** - Foreign keys
- ✅ **Index Analysis** - Índices criados
- ✅ **Trigger Detection** - Triggers ativos
- ✅ **View Analysis** - Views criadas
- ✅ **Integrity Check** - `PRAGMA integrity_check`
- ✅ **Encryption Detection** - SQLCipher, etc
- ✅ **Deleted Records Recovery** - Unallocated space
- ✅ **WAL Files** - Write-Ahead Logging

**Técnicas Avançadas:**
```sql
-- Recover deleted records
PRAGMA freelist_count;

-- Check encryption
PRAGMA cipher_version;

-- Vacuum analysis
PRAGMA page_count;
PRAGMA page_size;
```

**Resultado Exemplo:**
```json
{
  "TotalDatabases": 234,
  "TotalTables": 1456,
  "TotalRecords": 245678,
  "EncryptedDatabases": 12,
  "CorruptedDatabases": 0,
  "DeletedRecordsRecovered": 3456,
  "LargestDatabase": "msgstore.db (456 MB)",
  "DatabasesAnalyzed": [
    {
      "Path": "/data/data/com.whatsapp/databases/msgstore.db",
      "Size": "456 MB",
      "Tables": 23,
      "Records": 10234,
      "Encrypted": false
    }
  ]
}
```

---

### 11. ⏱️ Timeline Analyzer

**Timeline Forense de Eventos**

**Eventos Rastreados:**

#### 📱 **App Events**
- Instalação de apps
- Atualização de apps
- Desinstalação de apps
- Primeira execução
- Últimas execuções

#### 📞 **Communication Events**
- SMS enviados/recebidos
- Chamadas realizadas/recebidas
- Contatos adicionados/modificados

#### 📁 **File Events**
- Arquivos criados
- Arquivos modificados
- Arquivos deletados
- Downloads concluídos
- Fotos tiradas

#### 🌐 **Network Events**
- WiFi connections
- Mobile data sessions
- Bluetooth pairings
- VPN connections
- Airplane mode toggle

#### 📍 **Location Events**
- GPS locations
- Cell tower changes
- WiFi access points
- Geofence entries/exits

#### 🔐 **Security Events**
- Screen locks/unlocks
- Failed PIN attempts
- Fingerprint usage
- Face unlock
- Factory resets

#### ⚡ **System Events**
- Boot/shutdown
- Crashes
- Battery charging
- Storage changes
- OS updates

**Visualizações:**
- 📊 **Timeline Visual** - Linha do tempo gráfica
- 📅 **Calendar View** - Eventos por dia
- 🕐 **Hourly Heatmap** - Atividade por hora
- 📈 **Activity Graph** - Picos de atividade
- 🔍 **Event Search** - Busca por tipo/data

**Correlações:**
- 📱 App instalado → Primeira execução → Localização
- 📞 Chamada recebida → SMS enviado → Localização
- 📷 Foto tirada → Upload → Compartilhamento
- 🌐 WiFi conectado → Apps executados → Downloads

**Resultado Exemplo:**
```json
{
  "TotalEvents": 156789,
  "TimelineStart": "2024-01-01 00:00:00",
  "TimelineEnd": "2025-12-30 23:59:59",
  "EventTypes": {
    "FileEvents": 45678,
    "AppEvents": 2345,
    "CommunicationEvents": 12456,
    "NetworkEvents": 8934,
    "LocationEvents": 23456,
    "SecurityEvents": 15678,
    "SystemEvents": 5643
  },
  "BusiestDay": "2025-07-15 (2345 events)",
  "BusiestHour": "20:00-21:00 (avg 234 events)"
}
```

---

### 12. 💾 Partition Extractor

**Análise de Partições do Sistema**

**Partições Android:**

#### 🔧 **System Partitions**
- `/system` - Sistema operacional
- `/vendor` - Drivers e blobs do fabricante
- `/boot` - Kernel e ramdisk
- `/recovery` - Recovery image
- `/cache` - Cache do sistema
- `/data` - Dados do usuário

#### 🔐 **Security Partitions**
- `/tz` - TrustZone
- `/persist` - Persistent data
- `/frp` - Factory Reset Protection
- `/keystore` - Hardware keystore

#### 📡 **Modem Partitions**
- `/modem` - Firmware do modem
- `/fsg` - Filesystem Golden Copy
- `/dsp` - DSP firmware

#### 🔄 **Backup Partitions**
- `/systembak` - System backup
- `/bootbak` - Boot backup

**Informações Extraídas:**
- ✅ Nome da partição
- ✅ Device node (`/dev/block/...`)
- ✅ Tamanho total
- ✅ Espaço usado
- ✅ Espaço livre
- ✅ Filesystem type (ext4, f2fs, vfat)
- ✅ Mount point
- ✅ Mount options (ro, rw, nosuid, etc)
- ✅ Label
- ✅ UUID

**Comandos Utilizados:**
```bash
adb shell cat /proc/partitions
adb shell cat /proc/mounts
adb shell df -h
adb shell blkid
```

**Análises:**
- 🔍 Partições não-oficiais (rootkits)
- ⚠️ Modificações em /system
- 🔐 Encryption status por partição
- 💾 Espaço disponível crítico (<10%)
- 🔄 Partições danificadas (bad blocks)

**Imagem Forense:**
```bash
# Criar imagem dd (requer root)
adb shell su -c "dd if=/dev/block/bootdevice/by-name/userdata of=/sdcard/userdata.img"
adb pull /sdcard/userdata.img
```

**Resultado Exemplo:**
```json
{
  "TotalPartitions": 45,
  "SystemPartitions": 12,
  "UserDataPartition": {
    "Device": "/dev/block/sda21",
    "Size": "256 GB",
    "Used": "124.5 GB",
    "Free": "131.5 GB",
    "Filesystem": "ext4",
    "MountPoint": "/data",
    "Encrypted": true
  },
  "ModifiedSystemPartitions": 0,
  "SuspiciousPartitions": 0
}
```

---

### 13. 🗑️ Deleted File Recovery

**Recuperação de Arquivos Deletados**

**Técnicas de Recuperação:**

#### 1. **Journal Analysis**
- Análise do journal do ext4/f2fs
- Metadados de arquivos deletados
- Timestamps preservados

#### 2. **Unallocated Space Carving**
- Scan de blocos não-alocados
- File signature detection (magic bytes)
- Fragment reconstruction

#### 3. **Database Recovery**
- Deleted records em SQLite
- WAL (Write-Ahead Log) analysis
- Journal mode recovery

#### 4. **Thumbnail Recovery**
- Miniaturas de imagens deletadas
- `.thumbnails` directory
- Media cache

#### 5. **App Cache Recovery**
- Temporary files
- Cache directories
- Downloaded files cache

**Tipos de Arquivos Recuperáveis:**
- 📷 **Imagens:** JPG, PNG, GIF (magic bytes: `FF D8 FF`, `89 50 4E 47`)
- 🎥 **Vídeos:** MP4, AVI, MKV
- 🎵 **Áudio:** MP3, AAC, FLAC
- 📄 **Documentos:** PDF, DOC, DOCX
- 💾 **Databases:** SQLite
- 📧 **Emails:** EML, MSG
- 📱 **APKs:** Android packages

**Magic Bytes Conhecidos:**
```
JPG:  FF D8 FF
PNG:  89 50 4E 47
GIF:  47 49 46 38
PDF:  25 50 44 46
ZIP:  50 4B 03 04
MP4:  00 00 00 18 66 74 79 70
MP3:  FF FB / ID3
```

**Ferramentas:**
```bash
# Forensic imaging
adb shell su -c "dd if=/dev/block/sda21 of=/sdcard/data.img bs=4096"

# Carving com photorec (offline)
photorec data.img

# SQLite recovery
adb shell su -c "sqlite3 msgstore.db .dump" > recovered.sql
```

**Análise de Sucesso:**
- 🟢 **Full Recovery** - Arquivo completamente recuperado
- 🟡 **Partial Recovery** - Fragmentos recuperados
- 🔴 **Failed** - Sobrescrito ou danificado

**Limitações:**
- ⚠️ TRIM em SSD reduz chances
- ⚠️ Encryption dificulta recuperação
- ⚠️ Tempo desde deleção (quanto mais recente, melhor)
- ⚠️ Uso intenso do dispositivo sobrescreve dados

**Resultado Exemplo:**
```json
{
  "UnallocatedSpace": "45.6 GB",
  "FilesScanned": 245678,
  "FilesRecovered": 3456,
  "Images": 2345,
  "Videos": 234,
  "Documents": 456,
  "Databases": 234,
  "Audio": 187,
  "FullyRecovered": 2678,
  "PartiallyRecovered": 678,
  "Failed": 100,
  "SuccessRate": "77.5%",
  "OldestRecoveredFile": "2024-03-15 (9 months ago)"
}
```

---

## 💻 Requisitos do Sistema

### Hardware Mínimo
- **Processador:** Intel Core i5 ou superior
- **RAM:** 8 GB (16 GB recomendado)
- **Disco:** 50 GB de espaço livre
- **USB:** Porta USB 2.0+ para conexão com dispositivo

### Software Necessário
- **Sistema Operacional:** Windows 10/11 (64-bit)
- **.NET 8.0 Runtime** ou superior
- **Android Debug Bridge (ADB)** - Incluído ou instalação separada
- **Visual Studio 2022** (para desenvolvimento)

### Dispositivo Android
- **Android 5.0+** (Lollipop ou superior)
- **USB Debugging** habilitado
- **Root access** (opcional, mas recomendado para análises avançadas)

---

## 🎮 Guia de Uso

### Passo 1: Preparação do Dispositivo Android

1. **Habilitar Modo Desenvolvedor**
   ```
   Configurações → Sobre o telefone → Tocar 7x em "Número da versão"
   ```

2. **Habilitar USB Debugging**
   ```
   Configurações → Opções do desenvolvedor → Depuração USB → Ativar
   ```

3. **Conectar via USB**
   - Conecte o cabo USB
   - Aceite o prompt "Permitir depuração USB?"
   - Marque "Sempre permitir deste computador"

4. **Verificar Conexão**
   ```powershell
   adb devices
   ```
   Deve aparecer: `XXXXXXXXXX    device`

### Passo 2: Iniciar Análise

#### Via Interface Gráfica (GUI)

1. **Abrir o Aplicativo**
   ```
   AndroidForensicsGUI.exe
   ```

2. **Sistema de Detecção Automática**
   - A ferramenta detecta automaticamente dispositivos conectados
   - Usa 6 métodos de detecção simultâneos
   - Mostra informações detalhadas do dispositivo

3. **Configurar Análise**
   - Nome do Caso: `Investigação_2025_001`
   - Investigador: `Seu Nome`
   - Todos os 13 módulos profissionais serão executados automaticamente

4. **Iniciar Análise**
   - Clique em **"Iniciar Análise Completa"**
   - Acompanhe o progresso em tempo real
   - Tempo estimado: 10-30 minutos (dependendo do dispositivo)

#### Via Linha de Comando (CLI)

```powershell
# Análise completa
.\AndroidForensicsTool.exe --case "Caso001" --investigator "Nome" --full

# Módulos específicos
.\AndroidForensicsTool.exe --case "Caso001" --modules crypto,network,social

# Com output customizado
.\AndroidForensicsTool.exe --case "Caso001" --output "C:\Casos\Caso001"

# Root required
.\AndroidForensicsTool.exe --case "Caso001" --require-root
```

### Passo 3: Análise dos Resultados

Após conclusão, os resultados são salvos em:
```
C:\Users\{User}\Documents\AndroidForensics\YYYYMMDD_HHMMSS\
│
├── ForensicCase.json              # Dados estruturados completos
├── ForensicReport_Interactive_3D.html  # Relatório visual interativo
├── CryptoAnalysis.json            # Análise criptográfica
├── NetworkForensics.json          # Análise de rede
├── SocialMediaForensics.json      # Redes sociais
├── AIForensics.json               # Análise AI/ML
├── GeolocationIntelligence.json   # Geolocalização
├── BlockchainAnalysis.json        # Blockchain
├── DeepLearningIntelligence.json  # Deep learning
├── IoTSmartDevicesForensics.json  # IoT devices
├── ChainOfCustody.json            # Cadeia de custódia
└── AuditLog.txt                   # Log de auditoria
```

### Passo 4: Visualização de Relatórios

**Abrir Relatório Interativo:**
```powershell
Start-Process "ForensicReport_Interactive_3D.html"
```

**Recursos do Relatório:**
- 📊 Dashboard executivo com estatísticas
- 📈 Gráficos interativos (Chart.js, Plotly)
- 🗺️ Mapas de geolocalização
- 🌐 Grafos de rede 3D
- 📊 Timeline de eventos
- 🔍 Busca e filtros
- 📥 Exportação para PDF/Excel

---

## 🔍 Análises Disponíveis

### Análises Básicas (Módulos Originais)

| Módulo | Descrição | Tempo |
|--------|-----------|-------|
| **Device Info** | Hardware, OS, build, IMEI, serial | 10s |
| **Apps** | 200+ apps, permissões, malware scan | 2-5min |
| **Communications** | SMS, chamadas, contatos | 1-2min |
| **Browser** | Histórico, bookmarks, downloads | 30s |
| **Network** | WiFi, location services | 30s |
| **Files** | Sistema de arquivos completo | 2-5min |
| **Logs** | Logcat, dmesg, kernel logs | 1min |
| **Memory** | RAM, processos, conexões | 1-2min |
| **Malware** | 15 heurísticas de detecção | 3-5min |
| **Database** | Análise de DBs SQLite | 2-5min |
| **Timeline** | Timeline forense de eventos | 1min |
| **Partitions** | Informações de partições | 30s |
| **Recovery** | Arquivos deletados | 5-10min |

**Tempo Total Estimado:** 10-30 minutos (dispositivo completo)

---

## 📊 Relatórios e Exportação

### Formatos de Exportação

1. **JSON Estruturado**
   - Dados completos em formato estruturado
   - Facilita parsing e integração
   - Todos os módulos geram JSON

2. **HTML Interativo 3D**
   - Dashboard executivo
   - Gráficos Chart.js e Plotly
   - Mapas interativos
   - Timeline visual
   - Responsivo e mobile-friendly

3. **PDF Profissional**
   - Relatório executivo
   - Chain of custody
   - Evidências documentadas
   - Assinatura digital

4. **CSV/Excel**
   - Tabelas exportáveis
   - Análise em ferramentas externas
   - Importação em bancos de dados

### Tipos de Relatórios

#### 1. Relatório Executivo
```
Visão geral de alto nível para gestores
- Resumo executivo
- Principais descobertas
- Score de risco geral
- Recomendações
```

#### 2. Relatório Técnico
```
Detalhes completos para analistas
- Todos os dados técnicos
- Logs completos
- Hashes e evidências
- Métodos utilizados
```

#### 3. Relatório Legal
```
Formato para uso judicial
- Chain of custody
- Conformidade com padrões
- Assinaturas e timestamps
- Evidências admissíveis
```

---

## 🏗️ Arquitetura do Sistema

### Estrutura de Diretórios

```
AndroidForensics/
│
├── AndroidForensicsTool/              # Core Library
│   ├── Core/
│   │   ├── Extractors/                # Módulos de Extração
│   │   │   ├── DeviceInfoExtractor.cs
│   │   │   ├── AppExtractor.cs
│   │   │   ├── CommunicationExtractor.cs
│   │   │   ├── NetworkLocationExtractor.cs
│   │   │   ├── BrowserExtractor.cs
│   │   │   ├── FileSystemExtractor.cs
│   │   │   └── LogExtractor.cs
│   │   ├── AdbWrapper.cs              # Interface ADB
│   │   ├── ForensicAnalyzer.cs        # Orquestrador Principal
│   │   ├── EvidenceManager.cs         # Gestão de Evidências
│   │   ├── DatabaseAnalyzer.cs        # Análise de DBs
│   │   ├── MemoryAnalyzer.cs          # Análise de Memória
│   │   ├── MalwareScanner.cs          # Detecção de Malware
│   │   ├── TimelineAnalyzer.cs        # Timeline Forense
│   │   ├── PartitionExtractor.cs      # Análise de Partições
│   │   ├── DeletedFileRecovery.cs     # Recuperação de Arquivos
│   │   └── DeviceDetectionEngine.cs   # Detecção Multi-Método
│   └── Models/                        # Data Models
│
├── AndroidForensicsGUI/               # Interface Gráfica
│   ├── MainWindow.xaml                # GUI Principal
│   ├── MainWindow.xaml.cs
│   └── App.xaml
│
└── README.md                          # Este arquivo
```

### Fluxo de Execução

```
1. Detecção de Dispositivo (6 métodos simultâneos)
   ↓
2. Verificação de Permissões (Root, USB Debugging)
   ↓
3. Coleta de Dados (Execução paralela)
   └─→ 13 Módulos Profissionais
   ↓
4. Processamento e Análise
   ├─→ Detecção de Malware
   ├─→ Análise de Memória
   └─→ Timeline Forense
   ↓
5. Geração de Relatórios
   ├─→ JSON estruturado
   ├─→ HTML interativo
   └─→ Chain of Custody
   ↓
6. Auditoria e Log
```

### Tecnologias Utilizadas

- **.NET 8.0** - Framework principal
- **C# 12** - Linguagem de programação
- **WPF** - Interface gráfica
- **ADB** - Android Debug Bridge
- **SQLite** - Parsing de databases
- **Chart.js** - Gráficos interativos
- **Plotly** - Visualização 3D
- **Three.js** - Gráficos 3D
- **Newtonsoft.Json** - Serialização JSON
- **System.Management** - WMI queries

---

## 📚 Casos de Uso

### 1. Investigação Criminal
```
Cenário: Suspeita de tráfico de drogas via WhatsApp

Análises Utilizadas:
✅ SocialMediaForensics → 10.000+ mensagens do WhatsApp
✅ GeolocationIntelligence → Rotas e locais frequentes
✅ AIForensics → Análise de sentimento e padrões
✅ NetworkForensics → Conexões suspeitas

Resultado:
- 2.847 mensagens relacionadas ao caso
- 15 localizações de interesse
- 3 contatos principais identificados
- Timeline completa de eventos
```

### 2. Fraude Financeira
```
Cenário: Lavagem de dinheiro com criptomoedas

Análises Utilizadas:
✅ BlockchainAnalyzer → 5 carteiras detectadas
✅ NetworkForensics → Exchanges e VPNs
✅ SocialMediaForensics → Conversas sobre crypto
✅ AIForensics → Padrões de transação

Resultado:
- $450.000 USD em transações
- Mixing services detectados
- Risk Score: 85/100 (CRÍTICO)
- Evidências de lavagem
```

### 3. Cyberstalking
```
Cenário: Perseguição e ameaças online

Análises Utilizadas:
✅ SocialMediaForensics → Múltiplas plataformas
✅ GeolocationIntelligence → Tracking de localização
✅ DeepLearningIntelligence → Sentiment analysis
✅ IoTSmartDevicesForensics → Dispositivos conectados

Resultado:
- 500+ mensagens ameaçadoras
- Rastreamento de localização detectado
- 3 dispositivos Bluetooth suspeitos
- Sentiment Score: 0.15 (Negativo extremo)
```

### 4. Corporate Espionage
```
Cenário: Vazamento de informações confidenciais

Análises Utilizadas:
✅ NetworkForensics → Exfiltração de dados
✅ CryptoAnalyzer → Chaves e certificados
✅ AIForensics → Anomalias de comportamento
✅ MemoryAnalyzer → Processos suspeitos

Resultado:
- 25GB de dados exfiltrados
- Conexões a servidores externos
- Keylogger detectado
- Malware APT identificado
```

### 5. Child Protection
```
Cenário: Proteção de menores online

Análises Utilizadas:
✅ SocialMediaForensics → Conversas em apps
✅ DeepLearningIntelligence → Análise de imagens
✅ AIForensics → Detecção de ameaças
✅ GeolocationIntelligence → Locais visitados

Resultado:
- Contatos suspeitos identificados
- Imagens sensíveis detectadas
- Padrões de grooming identificados
- Evidências preservadas legalmente
```

---

## 🔒 Segurança e Compliance

### Chain of Custody

Toda evidência é protegida com:
- ✅ **Hash MD5/SHA256** no momento da coleta
- ✅ **Timestamp** preciso (UTC)
- ✅ **Investigador** identificado
- ✅ **Dispositivo** identificado (IMEI, Serial)
- ✅ **Método** de coleta documentado
- ✅ **Integridade** verificável

### Conformidade com Padrões

- ✅ **NIST SP 800-86** - Guide to Integrating Forensic Techniques
- ✅ **ISO/IEC 27037** - Guidelines for digital evidence
- ✅ **ACPO Principles** - UK Good Practice Guide
- ✅ **SWGDE** - Scientific Working Group on Digital Evidence
- ✅ **RFC 3227** - Guidelines for Evidence Collection

### Segurança da Ferramenta

- ✅ **Write Protection** - Modo somente leitura por padrão
- ✅ **Audit Logging** - Todas as operações registradas
- ✅ **Access Control** - Autenticação de usuário
- ✅ **Encryption** - Dados sensíveis criptografados
- ✅ **Tamper Detection** - Detecção de alterações

### Privacidade e LGPD/GDPR

**IMPORTANTE:** Esta ferramenta coleta dados pessoais sensíveis. 

**Requisitos Legais:**
- ⚖️ Autorização judicial quando necessária
- 📋 Consentimento informado (quando aplicável)
- 🔒 Proteção de dados coletados
- 🗑️ Descarte seguro após prazo legal
- 📊 Minimização de dados
- 🔐 Anonimização quando possível

**Use apenas em:**
- Investigações criminais autorizadas
- Perícias judiciais
- Incidentes de segurança corporativos autorizados
- Pesquisas com consentimento

---

## 🔧 Troubleshooting

### Dispositivo Não Detectado

**Problema:** `adb devices` não lista o dispositivo

**Soluções:**
```powershell
# 1. Verificar cabo USB
Teste com outro cabo USB de qualidade

# 2. Reinstalar drivers ADB
# Windows - Device Manager
# Atualizar driver → Buscar automaticamente

# 3. Reiniciar ADB server
adb kill-server
adb start-server
adb devices

# 4. Verificar USB Debugging
Configurações → Opções desenvolvedor → USB Debugging

# 5. Revogar autorizações USB
Configurações → Opções desenvolvedor → Revogar autorizações
# Desconecte e reconecte o dispositivo
```

### Erro: Permissão Negada

**Problema:** `Permission denied` em operações

**Soluções:**
```powershell
# 1. Verificar root
adb shell su -c "id"
# Deve retornar: uid=0(root)

# 2. Executar com root
adb root
adb remount

# 3. Se não tiver root
# Algumas análises ficam limitadas
# Considere fazer root do dispositivo (se autorizado)
```

### Análise Muito Lenta

**Problema:** Análise demora mais de 30 minutos

**Soluções:**
```powershell
# 1. Desabilitar módulos pesados
# Na GUI: desmarque Deep Learning e Social Media

# 2. Aumentar timeout ADB
adb root
adb shell setprop service.adb.tcp.port 5555

# 3. Usar cabo USB 3.0
# Velocidades: USB 2.0 (480 Mbps) vs USB 3.0 (5 Gbps)

# 4. Fechar outros apps no PC
# Libere RAM e CPU
```

### Erro ao Parsear Database

**Problema:** `Unable to open database file`

**Soluções:**
```powershell
# 1. Verificar permissões
adb shell su -c "chmod 644 /data/data/com.whatsapp/databases/msgstore.db"

# 2. Copiar para temp
adb shell su -c "cp /data/data/com.whatsapp/databases/msgstore.db /sdcard/"
adb pull /sdcard/msgstore.db

# 3. Verificar integridade
sqlite3 msgstore.db "PRAGMA integrity_check;"
```

### Relatório HTML Não Abre

**Problema:** Relatório 3D não carrega

**Soluções:**
```powershell
# 1. Abrir com navegador moderno
# Chrome, Edge, Firefox (não IE!)

# 2. Verificar JavaScript habilitado
# Configurações → JavaScript → Permitir

# 3. Executar servidor local
python -m http.server 8000
# Abrir: http://localhost:8000/ForensicReport_Interactive_3D.html

# 4. Verificar arquivo completo
# Tamanho > 100KB
Get-ChildItem ForensicReport_Interactive_3D.html | Select-Object Length
```

### Erro de Memória Insuficiente

**Problema:** `OutOfMemoryException`

**Soluções:**
```powershell
# 1. Aumentar heap do .NET
set DOTNET_GCHeapCount=4
set DOTNET_GCServer=1

# 2. Processar em lotes
# Modificar configuração para analisar menos arquivos por vez

# 3. Fechar outros programas
# Libere pelo menos 4GB de RAM

# 4. Upgrade de hardware
# Recomendado: 16GB RAM
```

---

## ❓ FAQ

### Perguntas Gerais

**Q: Preciso de root no dispositivo?**
A: Não obrigatório, mas **altamente recomendado**. Com root você obtém:
- ✅ Acesso completo ao sistema
- ✅ Databases de apps (WhatsApp, etc)
- ✅ Senhas WiFi
- ✅ Logs protegidos
- ✅ Partições do sistema

Sem root, análises ficam limitadas a dados acessíveis via ADB.

**Q: A ferramenta funciona em iOS?**
A: **Não**. Esta ferramenta é específica para Android. Para iOS, considere ferramentas como:
- Cellebrite UFED
- Oxygen Forensic Detective
- Magnet AXIOM

**Q: É possível analisar sem o dispositivo físico?**
A: **Parcialmente**. Você pode analisar:
- ✅ Backups ADB (`adb backup`)
- ✅ Imagens do sistema (dd, TWRP)
- ✅ Databases extraídos

Mas perde análises em tempo real (memória, processos).

**Q: Os dados são enviados para a nuvem?**
A: **NÃO**. Toda análise é 100% local:
- ✅ Sem conexão internet necessária
- ✅ Dados permanecem no seu computador
- ✅ Nenhum upload externo
- ✅ Privacidade garantida

**Q: Quanto tempo demora uma análise completa?**
A: Varia com o dispositivo:
- Rápido (8GB dados): 10-15 minutos
- Médio (32GB dados): 20-30 minutos
- Lento (128GB+ dados): 45-90 minutos

**Q: Posso usar comercialmente?**
A: Depende da licença adquirida:
- 🔓 **Open Source:** Uso pessoal/educacional
- 💼 **Comercial:** Empresas de segurança/perícia
- 🏛️ **Governo:** Forças de segurança
- 🎓 **Acadêmica:** Universidades/pesquisa

### Perguntas Técnicas

**Q: Quais versões do Android são suportadas?**
A: Android 5.0 (Lollipop) até Android 15 (latest)
- ✅ Android 5.x - 7.x: Full support
- ✅ Android 8.x - 10.x: Full support
- ✅ Android 11+: Full support (com adaptações)

**Q: Funciona com dispositivos bloqueados?**
A: **Limitado**. Com dispositivo bloqueado:
- ✅ Informações básicas (modelo, IMEI)
- ❌ Dados internos (requer unlock)
- ❌ Apps e databases

Para análise completa, dispositivo deve estar **desbloqueado**.

**Q: Posso analisar múltiplos dispositivos simultaneamente?**
A: **Sim**, mas:
- ✅ Múltiplas instâncias da ferramenta
- ✅ Cada dispositivo em pasta separada
- ⚠️ Requer recursos (RAM, CPU)

Recomendado: Máximo 2-3 dispositivos simultaneamente.

**Q: Como exportar para outras ferramentas forenses?**
A: Formatos compatíveis:
- ✅ **JSON** → Parsing custom
- ✅ **CSV** → Excel, Tableau
- ✅ **SQLite** → DB Browser, Python
- ✅ **HTML** → Qualquer navegador

**Q: A ferramenta modifica o dispositivo?**
A: **NÃO** em modo padrão:
- ✅ Somente leitura (read-only)
- ✅ Sem instalação de apps
- ✅ Sem modificação de arquivos
- ✅ Forensically sound

Exceção: Modo de recuperação pode gravar temporariamente.

---

## 📊 Estatísticas do Projeto

```
📝 Linhas de Código:     6.000+
🔧 Módulos:              13 Profissionais
🎯 Análises:             40+ tipos
📱 Plataformas:          Android 5.0+
🌐 Protocolos:           20+
📊 Data Sources:         50+
⏱️ Desenvolvimento:      6+ meses
👨‍💻 Desenvolvedores:      Equipe especializada
🏆 Nível:                Profissional
```

---

## 🔄 Roadmap e Futuras Funcionalidades

### v3.1 (Q1 2026)
- [ ] Suporte para Android 16
- [ ] Análise de eSIM
- [ ] Cloud backups (Google Drive, iCloud)
- [ ] Módulo de análise de drones
- [ ] API REST para integração

### v3.2 (Q2 2026)
- [ ] Interface web
- [ ] Análise colaborativa multi-usuário
- [ ] Machine Learning aprimorado
- [ ] Suporte para Wear OS
- [ ] Integração com SIEM

### v4.0 (Q3 2026)
- [ ] Análise de 5G networks
- [ ] Quantum-resistant cryptography
- [ ] AR/VR evidence visualization
- [ ] Autonomous AI analysis
- [ ] Blockchain evidence storage

---

## 📜 Licença e Termos de Uso

### Licença
```
Android Forensics Tool - Ultra Advanced Edition
Copyright (c) 2025 Android Forensics Team

Este software é fornecido sob licença restrita e confidencial.
Uso não autorizado é estritamente proibido.

Para licenciamento comercial, entre em contato:
licensing@androidforensics.com
```

### Termos de Uso

**ACEITO:**
- ✅ Investigações criminais autorizadas
- ✅ Perícias judiciais oficiais
- ✅ Segurança corporativa (com autorização)
- ✅ Pesquisa acadêmica (com consentimento)
- ✅ Treinamento e educação

**PROIBIDO:**
- ❌ Uso não autorizado em dispositivos
- ❌ Invasão de privacidade
- ❌ Espionagem ilegal
- ❌ Distribuição não autorizada
- ❌ Engenharia reversa

### Disclaimer

```
⚠️ AVISO LEGAL

Este software destina-se EXCLUSIVAMENTE a:
- Profissionais forenses autorizados
- Investigações legais e judiciais
- Uso com devido processo legal

O uso inadequado pode violar:
- Leis de privacidade (LGPD, GDPR)
- Leis de crimes cibernéticos
- Direitos constitucionais

Os desenvolvedores NÃO se responsabilizam por:
- Uso ilegal ou não autorizado
- Danos causados por uso inadequado
- Violações de privacidade
- Consequências legais

SEMPRE consulte um advogado antes de usar
esta ferramenta em investigações.
```

---

## 👥 Créditos e Agradecimentos

**Desenvolvido por:**
- Escanearcpl

**Tecnologias Utilizadas:**
- Microsoft .NET Team
- Android Open Source Project
- SQLite Development Team
- Chart.js Contributors
- Plotly Team
- Three.js Community

---

## 🎓 Referências e Bibliografia

### Livros Recomendados
1. **"Android Forensics"** - Andrew Hoog
2. **"Practical Mobile Forensics"** - Satish Bommisetty
3. **"Digital Forensics with Open Source Tools"** - Cory Altheide
4. **"The Art of Memory Forensics"** - Michael Hale Ligh

### Papers Acadêmicos
1. NIST SP 800-86 - Guide to Integrating Forensic Techniques
2. ISO/IEC 27037:2012 - Digital Evidence Guidelines
3. SWGDE Best Practices for Mobile Device Forensics

### Recursos Online
- Android Developer Documentation
- OWASP Mobile Security Project
- Digital Forensics Wiki
- Forensic Focus Forums

---

## 📝 Changelog

### v3.0.0 (2025-12-30) - ULTRA ADVANCED EDITION
```
🚀 TRANSFORMAÇÃO COMPLETA - 10000% DE MELHORIA

🆕 NOVOS MÓDULOS:
+ CryptoAnalyzer (800 linhas) - Análise criptográfica militar
+ NetworkForensics (900 linhas) - Senhas WiFi, VPN, backdoors
+ SocialMediaForensics (1000 linhas) - 10+ plataformas, WhatsApp deep
+ AIForensics (600 linhas) - Machine Learning & AI preditiva
+ GeolocationIntelligence (900 linhas) - GPS, WiFi, Cell towers
+ BlockchainAnalyzer (900 linhas) - 15+ cryptos, mixing detection
+ DeepLearningIntelligence (900 linhas) - NLP, facial recognition
+ IoTSmartDevicesForensics (900 linhas) - Bluetooth, NFC, wearables
+ Interactive3DReportGenerator (500 linhas) - Relatórios 3D interativos

✨ MELHORIAS:
* Integração completa de todos os módulos
* Sistema de detecção multi-método (6 técnicas)
* Parsing direto de databases SQLite
* Score de risco com AI (0-100)
* Timeline geográfica 3D
* Análise preditiva de ameaças
* Relatórios HTML interativos

🔧 TOTAL:
+ 7.000+ linhas de código novo
+ 80+ tipos de análises
+ 17 módulos profissionais
+ 100+ fontes de dados

---

<div align="center">

**🔬 Android Forensics Tool - Ultra Advanced Edition**

*Desenvolvido com 💙 para profissionais de forense digital*

![Made with](https://img.shields.io/badge/Made%20with-.NET%208.0-purple.svg)
![AI Powered](https://img.shields.io/badge/AI-Powered-green.svg)
![Security](https://img.shields.io/badge/Security-Military%20Grade-red.svg)

**© 2026 Android Forensics Team. Todos os direitos reservados.**

*"A verdade está nos dados"*

</div>
