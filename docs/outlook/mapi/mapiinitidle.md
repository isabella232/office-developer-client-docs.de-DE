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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e4f4cdd1d0ed2e03d49f471e6e91464b7973c920
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793124"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**Betrifft**: Outlook 
  
Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Parameter

 _lpvReserved_
  
> [in] Reserviert. NULL muss sein.
    
## <a name="return-value"></a>R�ckgabewert

Die **MAPIInitIdle** -Funktion gibt NULL zurück, falls die Initialisierung erfolgreich ist, und 1 ist. Wenn **MAPIInitIdle** mehrere Male aufgerufen wird, alle zusätzlichen Anrufe fehlerfrei ausgeführt werden, jedoch werden ignoriert, außer wenn erhöht den Referenzzähler. 
  
## <a name="remarks"></a>Bemerkungen

Eine Clientanwendung oder Dienstanbieter muss **MAPIInitIdle** aufrufen, bevor alle anderen im Leerlauf Engine-Funktion aufgerufen. 
  
Jedem Aufruf von **MAPIInitIdle** muss durch einen nachfolgenden Aufruf von [MAPIDeInitIdle](mapideinitidle.md)abgeglichen werden, oder das Modul im Leerlauf verläuft von Links für die aufrufende Anwendung ausgeführt. 
  
Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp: 
  
|**Im Leerlauf routinemäßige-Funktion**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Eigenschaften einer registrierten im Leerlauf Routine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.  <br/> |
|**MAPIInitIdle** <br/> |Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.  <br/> |
   
Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist. Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität. 
  

