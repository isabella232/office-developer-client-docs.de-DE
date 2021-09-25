---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2451601d50fc17328a5162d38d4a17a0e800a27d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610118"
---
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die **MAPICrashRecovery-Funktion** überprüft den Status des freigegebenen Arbeitsspeichers für die Persönliche Ordner-Datei (PST) oder die Offlineordnerdatei (OST). Wenn sich der Speicher in einem konsistenten Zustand befindet, verschiebt die **MAPICrashRecovery-Funktion** die Daten auf den Datenträger und verhindert weiteren Lese- oder Schreibzugriff, bis der Prozess beendet wird. 
  
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
  
> [in] Flags, die verwendet werden, um zu steuern, wie die MAPI-Absturzwiederherstellung ausgeführt wird. Die folgenden Flags können festgelegt werden:
    
   - **MAPICRASH \_ RECOVER:** Wenn sich die PSTs oder OSTs in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und sperren Sie die PSTs oder OSTs, um Lese- oder Schreibzugriff zu verhindern.
    
   - **MAPICRASH \_ CONTINUE:** Entsperren Sie die PSTs oder OSTs für das Debuggen. Rufen Sie nach einem erfolgreichen Aufruf von **MAPICrashRecovery** mit dem **Flag MAPICRASH_RECOVER** **MAPICrashRecovery** mit dem **MAPICRASH \_ CONTINUE-Flag** auf, damit das Debuggen fortgesetzt werden kann. 
    
   - **MAPICRASH \_ SYSTEM_SHUTDOWN:** Wenn sich die PSTs oder OSTs in einem konsistenten Zustand befinden, verschieben Sie die Daten auf den Datenträger, und sperren Sie die PSTs oder OSTs, um Lese- oder Schreibzugriff zu verhindern. PsTs oder OSTs können nicht mit **MAPICRASH \_ CONTINUE** entsperrt werden. Muss in Kombination mit **MAPICRASH \_ RECOVER** verwendet werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Das obere Byte (0xFF000000) ist für anbieterspezifische Absturzwiederherstellungsflags reserviert.
  
Rufen Sie **MAPICrashRecovery** mit den **MAPICRASH \_ RECOVER-** und **MAPICRASH_SYSTEM_SHUTDOWN-Flags** als Reaktion auf die **WM_ENDSESSION** Nachricht auf. 
  
## <a name="see-also"></a>Siehe auch

- [Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz](about-the-mapi-crash-recovery-api.md)
- [Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz](how-to-use-the-mapi-crash-recovery-api.md)

