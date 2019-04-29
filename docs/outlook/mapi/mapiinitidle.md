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
  
Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Parameter

 _lpvReserved_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>Rückgabewert

Die **MAPIInitIdle** -Funktion gibt NULL zurück, wenn die Initialisierung erfolgreich ist, und 1 andernfalls. Wenn **MAPIInitIdle** mehrmals aufgerufen wird, werden alle zusätzlichen Aufrufe erfolgreich ausgeführt, werden jedoch ignoriert, außer um den Verweiszähler zu erhöhen. 
  
## <a name="remarks"></a>Bemerkungen

Eine Clientanwendung oder ein Dienstanbieter muss **MAPIInitIdle** aufrufen, bevor eine andere Leerlauf Funktion des Moduls aufgerufen wird. 
  
Jeder Aufruf von **MAPIInitIdle** muss durch einen nachfolgenden Aufruf von [MAPIDeInitIdle](mapideinitidle.md)oder das Leerlauf Modul für die aufrufende Anwendung ausgeführt werden. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem [FNIDLE](fnidle.md) -Funktionsprototyp basieren: 
  
|**Leerlauf Routine Funktion**|**Verwendung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Eigenschaften einer registrierten Leerlauf Routine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.  <br/> |
|**MAPIInitIdle** <br/> |Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.  <br/> |
   
Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität. 
  

