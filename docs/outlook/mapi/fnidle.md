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
  
Definiert eine Leerlauf Routine, die vom MAPI-Leerlauf Modul regelmäßig gemäß der Priorität aufgerufen wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI  <br/> |
|EntSprechender Zeigertyp:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameter

 _lpvContext_
  
> in Zeiger auf einen Speicherblock, der von MAPI bei jedem Aufruf an die Leerlauf Routine übergeben wird. Dieser Zeiger wird im _pvIdleParam_ -Parameter von [FTGREGISTERIDLEROUTINE](ftgregisteridleroutine.md)an das MAPI-Leerlauf Modul übergeben. Die Daten im Speicherblock können Kontext für den Aufruf der Leerlauf Routine bereitstellen, beispielsweise das zu verwendende Objekt oder den aktuellen Status eines langwierigen Vorgangs.
    
## <a name="return-value"></a>Rückgabewert

FALSE 
  
> Eine Leerlauf Routine mit dem **FNIDLE** -Prototyp sollte immer false zurückgeben. 
    
## <a name="remarks"></a>Bemerkungen

Die spezifische Funktionalität der Leerlauf Routine wird von der implementierenden Clientanwendung oder dem Dienstanbieter bestimmt. 
  
Der Client oder Anbieter muss die Ausführungszeit der einzelnen Zustände einer Leerlauf Routine einschränken. Jeder Status sollte eine minimale Verarbeitung durchführen, den aktuellen Status in den Kontextdaten aktualisieren, auf die von _lpvContext_verwiesen wird, und zum MAPI-Leerlauf Modul zurückkehren. 
  
Der Client oder Anbieter muss die MAPI-Funktion [MAPIInitIdle](mapiinitidle.md) aufrufen, bevor er seine eigene Leerlauf Routine mit einem Aufruf der [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) -Funktion registrieren kann. 
  
Die folgenden Funktionen befassen sich mit dem MAPI-Leerlauf Modul und mit Leerlauf Routinen, die auf dem FNIDLE-Funktionsprototyp basieren: 
  
|**Leerlauf Routine Funktion**|**Verwendung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Eigenschaften einer registrierten Leerlauf Routine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Deaktiviert oder aktiviert eine registrierte Leerlauf Routine, ohne Sie aus dem MAPI-System zu entfernen.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Fügt eine Leerlauf Routine zum MAPI-System hinzu, mit oder ohne Sie zu aktivieren.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Fährt das MAPI-Leerlauf Modul für die aufrufende Anwendung herunter.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das MAPI-Leerlauf Modul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** nehmen als Eingabeparameter das von **FtgRegisterIdleRoutine**zurückgegebene funktionstag an. 
  
Wenn alle Vordergrund Aufgaben für die Plattform inaktiv werden, ruft das MAPI-Leerlauf Modul die Leerlauf Routine mit der höchsten Priorität auf, die zur Ausführung bereit ist. Es gibt keine Garantie für die Anruf Reihenfolge unter Leerlauf Routinen mit derselben Priorität. 
  

