---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1e77d9a58256b240c45eb106aac1b030b91ee808
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567711"
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

 _Ftg_
  
> [in] Funktionstag, das die zu entfernende Leerlaufroutine identifiziert.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Jede Aufgabe in einer Clientanwendung oder einem Dienstanbieter kann jede Leerlaufroutine, für die sie über einen gültigen  _ftg-Parameter_ verfügt, aufheben. Insbesondere kann sich eine Leerlaufroutine selbst abmelden. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem [FNIDLE-Funktionsprototyp](fnidle.md) basieren: 
  
|**Routinefunktion "Leerlauf"**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|**DeregisterIdleRoutine** <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine erneut, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlaufroutine zum MAPI-System hinzu, mit oder ohne sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** verwenden als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag. 
  
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anrufreihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  
Nachdem die Leerlaufroutine aufgehoben wurde, ruft das Leerlaufmodul sie nicht mehr auf. Jede Implementierung, die **DeregisterIdleRoutine** aufruft, muss alle Speicherblöcke freigeben, an die Zeiger übergeben wurden, die das Leerlaufmodul im ursprünglichen Aufruf der **FtgRegisterIdleRoutine-Funktion** verwenden soll. 
  

