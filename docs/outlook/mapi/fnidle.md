---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412380"
---
# <a name="fnidle"></a>FNIDLE
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Leerlaufroutine, die das MAPI-Leerlaufmodul regelmäßig nach Priorität aufruft. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI  <br/> |
|Entsprechender Zeigertyp:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameter

 _lpvContext_
  
> [in] Zeiger auf einen Speicherblock, den MAPI bei jedem Aufruf an die Leerlaufroutine übergibt. Dieser Zeiger wird von [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)an das MAPI-Leerlaufmodul im _parameter pvIdleParam_ übergeben. Die Daten im Speicherblock können Kontext für den Aufruf der Leerlaufroutine bereitstellen, z. B. für das zu verwendende Objekt oder den aktuellen Status eines langwierigen Vorgangs.
    
## <a name="return-value"></a>Rückgabewert

FALSE 
  
> Eine Leerlaufroutine mit dem **FNIDLE-Prototyp** sollte immer FALSE zurückgeben. 
    
## <a name="remarks"></a>Hinweise

Die spezifische Funktionalität der Leerlaufroutine wird durch die implementierende Clientanwendung oder den Dienstanbieter bestimmt. 
  
Der Client oder Anbieter muss die Ausführungszeit jedes Zustands einer Leerlaufroutine begrenzen. Jeder Zustand sollte eine minimale Verarbeitungsmenge ausführen, den aktuellen Status in den Kontextdaten aktualisieren, auf die  _von lpvContext_ verwiesen wird, und zum MAPI-Leerlaufmodul zurückkehren. 
  
Der Client oder Anbieter muss die MAPI-Funktion [MAPIInitIdle](mapiinitidle.md) aufrufen, bevor er seine eigene Leerlaufroutine mit einem Aufruf der [FtgRegisterIdleRoutine-Funktion registrieren](ftgregisteridleroutine.md) kann. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlaufmodul und mit Leerlaufroutinen, die auf dem Prototyp der FNIDLE-Funktion basieren: 
  
|**Routinefunktion im Leerlauf**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Merkmale einer registrierten Leerlaufroutine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlaufroutine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlaufroutine, ohne sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt dem MAPI-System eine Leerlaufroutine mit oder ohne Aktivierung hinzu.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Beendet das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlaufmodul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine** zurückgegebene Funktionstag an. 
  
Wenn alle Vordergrundaufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlaufmodul die Leerlaufroutine mit der höchsten Priorität auf, die ausgeführt werden kann. Es gibt keine Garantie für das Aufrufen der Reihenfolge zwischen Leerlaufroutinen mit derselben Priorität. 
  

