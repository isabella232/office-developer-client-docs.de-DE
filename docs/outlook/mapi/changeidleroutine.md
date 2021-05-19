---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418267"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ändert einige oder alle Merkmale einer [FNIDLE-basierten](fnidle.md) Leerlaufroutine. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a>Parameter

_ftg_
  
> [in] Funktionstag, das die Leerlaufroutine identifiziert. 
    
_pfnIdle_
  
> [in] Zeiger auf die Leerlaufroutine. 
    
_pvIdleParam_
  
> [in] Zeiger auf einen neuen Speicherblock, der von der aufrufenden Implementierung für die Leerlaufroutine zugewiesen wird. 
    
_priIdle_
  
> [in] Wert, der eine neue Priorität für die Leerlaufroutine darstellt. Mögliche Prioritäten für implementierungsdefinierte Routinen sind größer oder kleiner als Null, aber nicht Null. Ein Wert von Null ist für ein Benutzerereignis reserviert, z. B. einen Mausklick oder eine WM_PAINT Nachricht. Werte, die größer als Null sind, stellen Prioritäten für Hintergrundaufgaben dar, die eine höhere Priorität als Benutzerereignisse haben und im Rahmen der standardmäßigen nachrichtenumpumpschleife Windows werden. Werte, die kleiner als Null sind, stellen Prioritäten für Leerlaufaufgaben dar, die nur während der Leerlaufzeit von Nachrichtenpumps ausgeführt werden. Beispiele für Prioritäten sind: 1 für die Vordergrundübermittlung, 1 für das Einfügen von Power-Edit-Zeichen und 3 für das Herunterladen neuer Nachrichten.
    
_csecIdle_
  
> [in] Eine neue Zeit in Hundertstel sekunden, um auf die Leerlaufroutine anzuwenden. Die Bedeutung des Anfänglichen Zeitwerts variiert, je nachdem, was im  _iroIdle-Parameter übergeben_ wird. Dies kann: 
    
  - Der Minimale Zeitraum der Untätigkeit des Benutzers, der verstreichen muss, bevor das MAPI-Leerlaufmodul die Leerlaufroutine zum ersten Mal aufruft, wenn das FIROWAIT-Flag in  _iroIdle_ festgelegt ist. Nach dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen. 
    
  - Das Mindestintervall zwischen Aufrufen der Leerlaufroutine, wenn das FIROINTERVAL-Flag in _iroIdle festgelegt ist._ 
    
_iroIdle_
  
> [in] Bitmaske mit Flags, die neue Optionen zum Aufrufen der Leerlaufroutine angeben. Genau eines der folgenden Kennzeichen muss festgelegt werden:
    
  - FIROINTERVAL: Die durch den  _csecIdle-Parameter_ angegebene Zeit ist das Mindestintervall zwischen aufeinander folgenden Aufrufen der Leerlaufroutine. 
      
  - FIROONCEONLY: Veraltet. Nicht verwenden. 
      
  - FIROPERBLOCK: Veraltet. Nicht verwenden. 
      
  - FIROWAIT: Die durch den  _csecIdle-Parameter_ angegebene Zeit ist die minimale Dauer der Untätigkeit des Benutzers, die verstreichen muss, bevor das #A0 die Leerlaufroutine zum ersten Mal aufruft. Nach dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen. 
    
_ircIdle_
  
> [in] Bitmaske von Flags, die verwendet werden, um die Änderungen an der Leerlaufroutine anzugeben. Die folgenden Flags können in beliebiger Kombination festgelegt werden:
    
  - FIRCCSEC: Eine Änderung der Zeit, die der Leerlaufroutine zugeordnet ist, d. h. eine Änderung, die durch den im  _csecIdle-Parameter_ übergebenen Wert angegeben wird. 
      
  - FIRCIRO: Eine Änderung der Optionen für die Leerlaufroutine, d. h. eine Änderung, die durch den im  _iroIdle-Parameter_ übergebenen Wert angegeben wird. 
      
  - FIRCPFN: Eine Änderung am Leerlaufroutinenzeiger, d. h. eine Änderung, die durch den im  _pfnIdle-Parameter übergebenen_ Wert angegeben wird. 
      
  - FIRCPRI: Eine Änderung an der Priorität der Leerlaufroutine, d. h. eine Änderung, die durch den im  _priIdle-Parameter_ übergebenen Wert angegeben wird. 
      
  - FIRCPV: Eine Änderung am Speicherblock der Leerlaufroutine, d. h. eine Änderung, die durch den im  _pvIdleParam-Parameter_ übergebenen Wert angegeben wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der [FNIDLE-Funktion](fnidle.md) basieren: 
  
|**Routinefunktion im Leerlauf**|**Nutzung**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag an. 
  
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann. Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  

