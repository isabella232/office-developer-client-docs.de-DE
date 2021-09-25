---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5721c4a99f6ead6fefa839b1c1e45fdd61d95c60
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567781"
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

_Ftg_
  
> [in] Funktionstag, das die Leerlaufroutine identifiziert. 
    
_pfnIdle_
  
> [in] Zeiger auf die Leerlaufroutine. 
    
_pvIdleParam_
  
> [in] Zeiger auf einen neuen Speicherblock, den die aufrufende Implementierung für die Leerlaufroutine zuweist. 
    
_priIdle_
  
> [in] Wert, der eine neue Priorität für die Leerlaufroutine darstellt. Mögliche Prioritäten für implementierungsdefinierte Routinen sind größer oder kleiner als Null, aber nicht Null. Der Wert Null ist für ein Benutzerereignis reserviert, z. B. ein Mausklick oder eine WM_PAINT Nachricht. Werte größer als Null stellen Prioritäten für Hintergrundaufgaben dar, die eine höhere Priorität als Benutzerereignisse haben und als Teil der Standardschleife Windows Nachricht verteilt werden. Werte kleiner als Null stellen Prioritäten für Leerlaufaufgaben dar, die nur während der Leerlaufzeit von Nachrichten ausgeführt werden. Beispiele für Prioritäten sind: 1 für die Vordergrundübermittlung, 1 für die Einfügung von Power-Edit-Zeichen und 3 zum Herunterladen neuer Nachrichten.
    
_csecIdle_
  
> [in] Eine neue Zeit in Hundertsteln einer Sekunde, die auf die Leerlaufroutine angewendet werden soll. Die Bedeutung des anfänglichen Zeitwerts variiert, je nachdem, was im  _iroIdle-Parameter_ übergeben wird. Dies kann folgende sein: 
    
  - Der minimale Zeitraum der Benutzerinaktivität, der verstrichen sein muss, bevor das MAPI-Leerlaufmodul zum ersten Mal die Leerlaufroutine aufruft, wenn das FIROWAIT-Flag in  _iroIdle_ festgelegt ist. Nach Ablauf dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen. 
    
  - Das minimale Intervall zwischen Aufrufen der Leerlaufroutine, wenn das FIROINTERVAL-Flag in  _iroIdle_ festgelegt ist. 
    
_iroIdle_
  
> [in] Bitmaske mit Flags, die neue Optionen für den Aufruf der Leerlaufroutine angeben. Es muss genau eines der folgenden Flags festgelegt werden:
    
  - FIROINTERVAL: Die durch den  _csecIdle-Parameter_ angegebene Zeit ist das minimale Intervall zwischen aufeinander folgenden Aufrufen der Leerlaufroutine. 
      
  - FIROONCEONLY: Veraltet. Nicht verwenden. 
      
  - FIROPERBLOCK: Veraltet. Nicht verwenden. 
      
  - FIROWAIT: Die durch den  _csecIdle-Parameter_ angegebene Zeit ist der minimale Zeitraum der Benutzerinaktivität, der verstrichen sein muss, bevor das MAPI-Leerlaufmodul zum ersten Mal die Leerlaufroutine aufruft. Nach Ablauf dieser Zeit kann das Leerlaufmodul die Leerlaufroutine so oft wie nötig aufrufen. 
    
_ircIdle_
  
> [in] Bitmaske von Flags, die verwendet werden, um die Änderungen anzugeben, die an der Leerlaufroutine vorgenommen werden sollen. Die folgenden Flags können in einer beliebigen Kombination festgelegt werden:
    
  - FIRCCSEC: Eine Änderung der Zeit, die der Leerlaufroutine zugeordnet ist, d. h. eine Änderung, die durch den im  _csecIdle-Parameter_ übergebenen Wert angegeben wird. 
      
  - FIRCIRO: Eine Änderung der Optionen für die Leerlaufroutine, d. h. eine Änderung, die durch den im  _iroIdle-Parameter_ übergebenen Wert angegeben wird. 
      
  - FIRCPFN: Eine Änderung am leerlaufaktiven Routinezeiger, d. h. eine Änderung, die durch den im  _parameter "pfnIdle"_ übergebenen Wert angegeben wird. 
      
  - FIRCPRI: Eine Änderung der Priorität der Leerlaufroutine, d. h. eine Änderung, die durch den im  _priIdle-Parameter_ übergebenen Wert angegeben wird. 
      
  - FIRCPV: Eine Änderung am Speicherblock der Leerlaufroutine, d. h. eine Änderung, die durch den im  _Parameter "pvIdleParam"_ übergebenen Wert angegeben wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem [FNIDLE-Funktionsprototyp](fnidle.md) basieren: 
  
|**Routinefunktion "Leerlauf"**|**Nutzung**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine erneut, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlaufroutine zum MAPI-System hinzu, mit oder ohne sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** verwenden als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag. 
  
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anrufreihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  

