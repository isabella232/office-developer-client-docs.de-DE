---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 070ae4c5381dd22e43ed92680c7d3db30c1352ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556742"
---
# <a name="fnidle"></a>FNIDLE
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Leerlaufroutine, die das MAPI-Leerlaufmodul regelmäßig gemäß der Priorität aufruft. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI  <br/> |
|Entsprechender Zeigertyp:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameter

 _lpvContext_
  
> [in] Zeiger auf einen Speicherblock, den mapi bei jedem Aufruf an die Leerlaufroutine übergibt. Dieser Zeiger wird an das MAPI-Leerlaufmodul im  _parameter pvIdleParam_ von [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)übergeben. Die Daten im Speicherblock können Kontext für den Aufruf der Leerlaufroutine bereitstellen, z. B. welches Objekt ausgeführt werden soll, oder den aktuellen Status eines längeren Vorgangs.
    
## <a name="return-value"></a>Rückgabewert

FALSE 
  
> Eine Leerlaufroutine mit dem **FNIDLE-Prototyp** sollte immer FALSE zurückgeben. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die spezifische Funktionalität der Leerlaufroutine wird von der implementierenden Clientanwendung oder dem Dienstanbieter bestimmt. 
  
Der Client oder Anbieter muss die Ausführungszeit jedes Zustands einer Leerlaufroutine begrenzen. Jeder Zustand sollte eine minimale Verarbeitung durchführen, den aktuellen Status in den Kontextdaten aktualisieren, auf die durch  _lpvContext_ verwiesen wird, und zum MAPI-Leerlaufmodul zurückkehren. 
  
Der Client oder Anbieter muss die MAPI-Funktion [MAPIInitIdle](mapiinitidle.md) aufrufen, bevor er seine eigene Leerlaufroutine mit einem Aufruf der [FtgRegisterIdleRoutine-Funktion](ftgregisteridleroutine.md) registrieren kann. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem FNIDLE-Funktionsprototyp basieren: 
  
|**Routinefunktion "Leerlauf"**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine erneut, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlaufroutine zum MAPI-System hinzu, mit oder ohne sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** verwenden als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag. 
  
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anrufreihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  

