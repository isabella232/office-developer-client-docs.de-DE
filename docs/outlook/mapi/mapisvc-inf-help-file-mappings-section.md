---
title: Abschnitt [Help File Mappings] in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62aee641-b73f-4f53-9e8d-adf010c9ea1a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91c69489e1a72c5cd702a3c4d0392220a89c38fd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580383"
---
# <a name="mapisvcinf-help-file-mappings-section"></a>Abschnitt [Help File Mappings] in MapiSvc.inf

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Im Abschnitt **[Help File Mappings]** enthält Einträge, dass jeweils eine Messagingdiensts die Datei zuzuordnen, die für Fehler, die vom Dienst bereitstellt. Einträge in diesem Abschnitt verwenden Sie das folgende Format: 
  
 **[Hilfe Dateizuordnungen]** _Nachricht Dienstname_  =   _Name der Hilfedatei_
  
Der Dienstname Nachricht ist der Name des Diensts installierten Nachricht. der Name der Hilfedatei ist der Name der Datei, in dem die Fehlerinformationen befindet. Im folgenden Beispiel zeigt einen typischen **[Help File Mappings]** -Abschnitt, der Einträge für drei Dienste enthält: MAPI, die MsgService-Dienst und das MS-Dienst. 
  
```cpp
[Help File Mappings]
MAPI=MAPI.HLP
MsgService=MYHELP.HLP
MS=STORE.HLP

```


