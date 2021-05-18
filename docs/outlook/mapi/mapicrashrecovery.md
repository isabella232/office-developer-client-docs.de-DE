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
  
Die **MAPICrashRecovery-Funktion** überprüft den Status des freigegebenen Speichers für persönliche Ordner (PST) oder Offlineordnerdatei (OST). Wenn sich der Arbeitsspeicher in einem konsistenten Zustand befindet, verschiebt die **MAPICrashRecovery-Funktion** die Daten auf den Datenträger und verhindert weiteren Lese- oder Schreibzugriff, bis der Prozess beendet wird. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |olmapi32.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> [in] Kennzeichen, die zum Steuern der Wiederherstellung der MAPI-Absturzwiederherstellung verwendet werden. Die folgenden Kennzeichen können festgelegt werden:
    
   - **MAPICRASH \_ RECOVER**: Wenn sich die PSTs oder OSTs in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und sperren Sie die PSTs oder OSTs, um den Lese- oder Schreibzugriff zu verhindern.
    
   - **MAPICRASH \_ CONTINUE**: Entsperren der PSTs oder OSTs zum Debuggen. Rufen Sie nach einem erfolgreichen Aufruf von **MAPICrashRecovery** mit dem **flag MAPICRASH_RECOVER** **MAPICrashRecovery** mit dem **MAPICRASH \_ CONTINUE-Flag** auf, um das Debuggen weiter zu ermöglichen. 
    
   - **MAPICRASH \_ SYSTEM_SHUTDOWN**: Wenn sich psTs oder OSTs in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und sperren Sie die PSTs oder OSTs, um den Lese- oder Schreibzugriff zu verhindern. Die PSTs oder OSTs können nicht mit **MAPICRASH CONTINUE entsperrt \_ werden.** Muss in Kombination mit **MAPICRASH \_ RECOVER verwendet werden.** 
    
## <a name="remarks"></a>Hinweise

Das obere Byte (0xFF000000) ist für anbieterspezifische Absturzwiederherstellungsflags reserviert.
  
Rufen **Sie MAPICrashRecovery** mit der **MAPICRASH \_ RECOVER** auf, **und MAPICRASH_SYSTEM_SHUTDOWN** als Antwort auf die WM_ENDSESSION werden.  
  
## <a name="see-also"></a>Siehe auch

- [Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz](about-the-mapi-crash-recovery-api.md)
- [Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz](how-to-use-the-mapi-crash-recovery-api.md)

