---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404561"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Entfernt eine [FNIDLE-basierte](fnidle.md) Leerlaufroutine aus dem MAPI-System. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Parameter

 _ftg_
  
> [in] Funktionstag, das die zu entfernende Leerlaufroutine identifiziert.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Jede Aufgabe in einer Clientanwendung oder einem Dienstanbieter kann alle Leerlaufroutinen, für die sie über einen gültigen  _ftg-Parameter_ verfügt, abmelden. Insbesondere kann sich eine Leerlaufroutine selbst abmelden. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der [FNIDLE-Funktion](fnidle.md) basieren: 
  
|**Routinefunktion im Leerlauf**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|**DeregisterIdleRoutine** <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag an. 
  
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann. Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  
Nachdem die Leerlaufroutine abgemeldet wurde, wird sie vom Leerlaufmodul nicht erneut aufruft. Jede Implementierung, die **DeregisterIdleRoutine** aufruft, muss alle Speicherblöcke, an die Zeiger für das Leerlaufmodul übergeben werden, für den ursprünglichen Aufruf der **FtgRegisterIdleRoutine-Funktion** übergeben werden. 
  

