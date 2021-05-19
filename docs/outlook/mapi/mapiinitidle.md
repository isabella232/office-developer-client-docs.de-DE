---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432443"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Parameter

 _lpvReserved_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

Die **MAPIInitIdle-Funktion** gibt null zurück, wenn die Initialisierung erfolgreich ist, und andernfalls 1. Wenn **MAPIInitIdle** mehrmals aufgerufen wird, sind alle zusätzlichen Aufrufe erfolgreich, werden jedoch ignoriert, außer, um die Referenzanzahl zu erhöhen. 
  
## <a name="remarks"></a>Hinweise

Eine Clientanwendung oder ein Dienstanbieter muss **MAPIInitIdle** aufrufen, bevor eine andere Im leerlaufmodulfunktion aufruft. 
  
Jedem Aufruf von **MAPIInitIdle** muss ein nachfolgender Aufruf von [MAPIDeInitIdle](mapideinitidle.md)entsprechen, oder das Leerlaufmodul wird für die aufrufende Anwendung noch ausgeführt. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der [FNIDLE-Funktion](fnidle.md) basieren: 
  
|**Routinefunktion im Leerlauf**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|**MAPIInitIdle** <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann. Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  

