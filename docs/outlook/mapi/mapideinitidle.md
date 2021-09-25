---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7c8bc1a38693f0bfc83d5d17cca1a1bb38f971de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556084"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a>Parameter

Keine. 
  
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung oder ein Dienstanbieter sollte **MAPIDeInitIdle** aufrufen, wenn das Leerlaufmodul nicht mehr benötigt wird, z. B. wenn die Verarbeitung beendet werden soll. 
  
Jeder Aufruf von [MAPIInitIdle](mapiinitidle.md) muss mit einem nachfolgenden Aufruf von **MAPIDeInitIdle** abgeglichen werden, andernfalls wird das Leerlaufmodul für die aufrufende Anwendung ausgeführt. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem [FNIDLE-Funktionsprototyp](fnidle.md) basieren: 
  
|**Routinefunktion "Leerlauf"**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine erneut, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlaufroutine zum MAPI-System hinzu, mit oder ohne sie zu aktivieren.  <br/> |
|**MAPIDeInitIdle** <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anrufreihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  

