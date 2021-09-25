---
title: EnableIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.EnableIdleRoutine
api_type:
- COM
ms.assetid: 332ea831-bdf9-4dbd-b9c7-a80f8ba11b3b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d81fec5072b51c26291b16253d0fefa5bfa89f91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567683"
---
# <a name="enableidleroutine"></a>EnableIdleRoutine

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktiviert oder deaktiviert eine [FNIDLE-basierte](fnidle.md) Leerlaufroutine. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
VOID EnableIdleRoutine(
  FTG ftg,
  BOOL fEnable
);
```

## <a name="parameters"></a>Parameter

 _Ftg_
  
> [in] Funktionstag, das die Leerlaufroutine angibt, die aktiviert oder deaktiviert werden soll. 
    
 _fEnable_
  
> [in] Enthält TRUE, wenn das Leerlaufmodul die Leerlaufroutine aktivieren soll, oder FALSE, wenn es deaktiviert werden soll.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem [FNIDLE-Funktionsprototyp](fnidle.md) basieren: 
  
|**Routinefunktion "Leerlauf"**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|**EnableIdleRoutine** <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine erneut, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlaufroutine zum MAPI-System hinzu, mit oder ohne sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** verwenden als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag. 
  
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anrufreihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  

