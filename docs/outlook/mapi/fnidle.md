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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bf1a84a1f305580fc9d9085753ab7eb5c62b8aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791716"
---
# <a name="fnidle"></a>FNIDLE
 
**Betrifft**: Outlook 
  
Definiert eine im Leerlauf-Routine, die das im Leerlauf MAPI-Modul in regelmäßigen Abständen nach Priorität aufruft. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI  <br/> |
|Zeigertyp des entsprechenden:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parameter

 _lpvContext_
  
> [in] Zeiger auf einen Block von Arbeitsspeicher, dass MAPI an im Leerlauf Routine übergeben es Zeit wird aufgerufen. Dieser Zeiger wird vom [FtgRegisterIdleRoutine](ftgregisteridleroutine.md)an das im Leerlauf MAPI-Modul in der _PvIdleParam_ -Parameter übergeben. Die Daten in den Arbeitsspeicher-Block können für den Anruf an die im Leerlauf Routine, beispielsweise zum Verarbeiten von, welches Objekt oder den aktuellen Status einer langen Operation Kontext bereitzustellen.
    
## <a name="return-value"></a>R�ckgabewert

FALSE 
  
> Eine im Leerlauf Routine mit dem Prototyp **FNIDLE** sollte immer FALSE zurück. 
    
## <a name="remarks"></a>Hinweise

Die spezifische Funktionen der der im Leerlauf Routine wird durch die Implementierung bestimmt Clientanwendung oder den Dienstanbieter. 
  
Der Client oder Anbieter muss die Ausführungszeit der einzelnen Zustände einer im Leerlauf Routine einschränken. Jeder Zustand sollte eine Mindest-Verarbeitung ausführen, in den Kontextdaten auf die _LpvContext_zeigt den aktuellen Status aktualisieren und zurück an die MAPI-Modul im Leerlauf. 
  
Der Client oder Anbieter muss die MAPI-Funktion [MAPIInitIdle](mapiinitidle.md) aufrufen, bevor sie eine eigene im Leerlauf Routine mit einem Aufruf der Funktion [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) registrieren kann. 
  
Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den FNIDLE Funktionsprototyp: 
  
|**Im Leerlauf routinemäßige-Funktion**|**Verwendung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Eigenschaften einer registrierten im Leerlauf Routine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** werden als Eingabeparameter das Function-Tag von **FtgRegisterIdleRoutine**zurückgegeben. 
  
Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist. Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität. 
  

