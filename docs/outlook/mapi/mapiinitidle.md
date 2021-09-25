---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 43b5168f1d29ead887f884e6c61456c5ab28364b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575484"
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

Die **MAPIInitIdle-Funktion** gibt null zurück, wenn die Initialisierung erfolgreich ist, andernfalls 1. Wenn **MAPIInitIdle** mehrmals aufgerufen wird, sind alle zusätzlichen Aufrufe erfolgreich, werden jedoch ignoriert, außer um die Referenzanzahl zu erhöhen. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung oder ein Dienstanbieter muss **MAPIInitIdle** aufrufen, bevor eine andere Leerlaufmodulfunktion aufgerufen wird. 
  
Jeder Aufruf von **MAPIInitIdle** muss mit einem nachfolgenden Aufruf von [MAPIDeInitIdle](mapideinitidle.md)abgeglichen werden, andernfalls wird das Leerlaufmodul für die aufrufende Anwendung ausgeführt. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem [FNIDLE-Funktionsprototyp](fnidle.md) basieren: 
  
|**Routinefunktion "Leerlauf"**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine erneut, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlaufroutine zum MAPI-System hinzu, mit oder ohne sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|**MAPIInitIdle** <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anrufreihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  

