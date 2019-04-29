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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407214"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die **MAPICrashRecovery** -Funktion überprüft den Status des freigegebenen Speichers (PST) oder der Offline Ordner Datei (Ost). Wenn sich der Speicher in einem konsistenten Zustand befindet, verschiebt die **MAPICrashRecovery** -Funktion die Daten auf den Datenträger und verhindert den weiteren Lese-oder Schreibzugriff, bis der Prozess beendet wird. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |olmapi32. dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> in Flags, die verwendet werden, um zu steuern, wie die MAPI-Crash Wiederherstellung ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
   - **MAPICRASH\_Recover**: Wenn sich die PST oder Kosten in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und Sperren Sie die PST oder Kosten, um Lese-oder Schreibzugriff zu verhindern.
    
   - **MAPICRASH\_Continue**: entsperren Sie die PST-oder Kosten für das Debugging. Rufen Sie nach einem erfolgreichen Aufruf von **MAPICrashRecovery** mit dem **MAPICRASH_RECOVER** -Flag **MAPICrashRecovery** mit dem Flag **MAPICRASH\_Continue** auf, um das Debuggen zu ermöglichen. 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: Wenn die PST oder Kosten sich in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und Sperren Sie die PST oder Kosten, um Lese-oder Schreibzugriff zu verhindern. Die PST oder Kosten kann nicht mit **MAPICRASH\_Continue**entsperrt werden. Muss in Kombination mit **MAPICRASH\_Recover**verwendet werden. 
    
## <a name="remarks"></a>Bemerkungen

Das obere Byte (0xFF000000) ist für anbieterspezifische Absturz Wiederherstellungs Kennzeichen reserviert.
  
Aufrufen von **MAPICrashRecovery** mit **den\_MAPICRASH Recover** -und **MAPICRASH_SYSTEM_SHUTDOWN** -Flags als Reaktion auf die **WM_ENDSESSION** -Nachricht. 
  
## <a name="see-also"></a>Siehe auch

- [Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz](about-the-mapi-crash-recovery-api.md)
- [Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz](how-to-use-the-mapi-crash-recovery-api.md)

