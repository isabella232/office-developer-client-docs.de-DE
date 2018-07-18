---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 22f17df9347b4744dfe6598e7007469ffb9e5251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793143"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Betrifft**: Outlook 
  
Die Funktion **MAPICrashRecovery** überprüft, ob der Zustand des Persönliche Ordner-Datei (PST) oder Offlineordnerdatei (OST) Arbeitsspeicher freigegeben. Wenn der Arbeitsspeicher in einen konsistenten Status befindet, wird die **MAPICrashRecovery** -Funktion verschiebt die Daten auf dem Datenträger und verhindert, dass weitere Lese- oder Schreibzugriff, bis der Prozess beendet wird. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Vom exportiert werden:  <br/> |olmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> [in] Kennzeichen, die steuern, wie die MAPI-Wiederherstellung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
   - **MAPICRASH\_wiederherstellen**: Wenn die PST-Dateien oder OSTs in einen konsistenten Status befinden, verschieben Sie die Daten auf dem Datenträger und die PST-Dateien oder OSTs, um zu verhindern, dass Lese- oder Schreibzugriff sperren.
    
   - **MAPICRASH\_weiter**: entsperren Sie die PST-Dateien oder OSTs für das debugging. Rufen Sie nach einem erfolgreichen Aufruf von **MAPICrashRecovery** mit dem **MAPICRASH_RECOVER** -Flag, **MAPICrashRecovery** mit der **MAPICRASH\_weiter** Kennzeichnung, damit das Debuggen, um den Vorgang fortzusetzen. 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: Wenn die PST-Dateien oder OSTs in einen konsistenten Status befinden, verschieben Sie die Daten auf dem Datenträger und die PST-Dateien oder OSTs, um zu verhindern, dass Lese- oder Schreibzugriff sperren. Die PST-Dateien oder OSTs kann nicht entsperrt mit werden **MAPICRASH\_weiter**. Muss verwendet werden, in Kombination mit **MAPICRASH\_wiederherstellen**. 
    
## <a name="remarks"></a>Bemerkungen

Das obere Byte (0xFF000000) ist für Anbieter für bestimmte Absturz Recovery Flags reserviert.
  
Rufen Sie **MAPICrashRecovery** mit der **MAPICRASH\_wiederherstellen** und **MAPICRASH_SYSTEM_SHUTDOWN** Flags als Antwort auf die Nachricht **WM_ENDSESSION** . 
  
## <a name="see-also"></a>Siehe auch

- [Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz](about-the-mapi-crash-recovery-api.md)
- [Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz](how-to-use-the-mapi-crash-recovery-api.md)

