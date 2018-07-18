---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791762"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**Betrifft**: Outlook 
  
Das MAPI-System hinzugefügt eine [FNIDLE](fnidle.md) funktionsbasierte im Leerlauf Routine. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a>Parameter

_pfnIdle_
  
> [in] Ein Zeiger auf die im Leerlauf Routine. 
    
_pvIdleParam_
  
> [in] Ein Zeiger auf einen Block von Arbeitsspeicher, die das Modul im Leerlauf sollte als Parameter für die im Leerlauf Routine beim übergeben es aufgerufen. 
    
_priIdle_
  
> [in] Die erste Priorität für die im Leerlauf Routine. Mögliche Prioritäten für die Implementierung definierten Routinen sind größer oder kleiner als 0 (null), aber nicht 0 (null). Die Priorität 0 (null) ist für eine Benutzerereignis wie klicken mit der Maus oder eine Nachricht WM_PAINT reserviert. Größer als 0 (null) Prioritäten darstellen Hintergrundaufgaben, die eine höhere Priorität als Veranstaltungen und werden im Rahmen der standardmäßigen Windows-Nachricht Pumpe Schleife verteilt. Prioritäten kleiner als 0 (null) darstellen im Leerlauf Aufgaben, die nur während der Nachricht Pumpe Leerlaufzeit ausgeführt. Beispiele für Prioritäten sind wie folgt: 1 für die Übermittlung von Vordergrund, für das Einfügen von Power bearbeiten Zeichen 2 und 3 für das Herunterladen von neuer Nachrichten.
    
_csecIdle_
  
> [in] Der Wert der anfänglichen Uhrzeit im Hundertstelsekunden, bei der Angabe im Leerlauf routinemäßige-Parameter verwendet werden. Die Bedeutung des ursprünglichen Zeitwerts hängt davon ab, was im _IroIdle_ -Parameter übergeben wird. Die Bedeutung kann eine der folgenden sein: 
    
  - Der Mindestzeitraum Untätigkeit für Benutzer, die verstreichen muss, bevor die MAPI ruft im Leerlauf Modul die im Leerlauf Routine zum ersten Mal, wenn das Flag FIROWAIT in _IroIdle_festgelegt ist. Nach der Übergabe diesmal, kann das Modul im Leerlauf die im Leerlauf Routine so oft wie nötig aufrufen. 
    
  - Das kürzeste Intervall zwischen Aufrufen der im Leerlauf Routine, wenn das Flag FIROINTERVAL in _IroIdle_festgelegt ist. 
    
_iroIdle_
  
> [in] Die Bitmaske Flags verwendet, um die anfängliche Optionen für die im Leerlauf Routine festgelegt. Die folgenden Kennzeichen können festgelegt werden:
    
  FIRONOADJUSTMENT
    
  > Verwenden Sie dieses Flag angegeben wird, dass der im Leerlauf routinemäßige Zeitgeber Standbymodus nicht angepasst werden sollten oder fortzusetzen. Das Standardverhalten ohne dieses Flag ist, dass beim Berechnen der verstrichenen Zeit Zeit für Ruhezustand ausgeschlossen wird. Wenn FIRONOADJUSTMENT übergeben wird, werden die Zeit für Ruhezustand eingeschlossen beim Berechnen der verstrichenen Zeit.
      
  FIRODISABLED
    
  > Die im Leerlauf Routine sollte deaktiviert werden, wenn registriert. Die Standardaktion besteht, die im Leerlauf Routine aktivieren, wenn **FtgRegisterIdleRoutine** registriert. 
      
  FIROINTERVAL 
    
  > Die durch den _CsecIdle_ -Parameter angegebenen Zeit ist das kürzeste Intervall zwischen aufeinander folgenden Aufrufen der Routine im Leerlauf. 
      
  FIROONCEONLY 
    
  > Veraltet. Nicht verwenden.  
      
  FIROPERBLOCK 
    
  > Veraltet. Nicht verwenden.  
      
  FIROWAIT 
    
  > Die durch den _CsecIdle_ -Parameter angegebenen Zeit ist der Mindestzeitraum Untätigkeit für Benutzer, die verstreichen muss, bevor das im Leerlauf MAPI-Modul die im Leerlauf Routine zum ersten Mal aufruft. Nach der Übergabe diesmal, kann das Modul im Leerlauf die im Leerlauf Routine so oft wie nötig aufrufen. 
    
## <a name="return-value"></a>R�ckgabewert

Die **FtgRegisterIdleRoutine** -Funktion gibt eine Function-Tag, identifiziert der im Leerlauf Routine, die die MAPI-System hinzugefügt wurde. Wenn **FtgRegisterIdleRoutine** nicht im Leerlauf Routine für die Clientanwendung oder Dienstanbieter registrieren können, beispielsweise aufgrund Speicherprobleme, wird NULL zurückgegeben. 
  
## <a name="remarks"></a>Bemerkungen

Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp. 
  
|**Im Leerlauf routinemäßige-Funktion**|**Nutzung**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Ändert die Eigenschaften einer registrierten im Leerlauf Routine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** werden als Eingabeparameter das Function-Tag von **FtgRegisterIdleRoutine**zurückgegeben. 
  
Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist. Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität. 
  
Es folgt ein Beispiel für das Flag FIRONOADJUSTMENT im _IroIdle_ -Parameter verwenden. 
  
1. Registrieren einer Routine im Leerlauf mit einer Verzögerung von 5 Minuten.
    
2. Ruhezustand/Standbymodus den Computer nach einer Minute (4 Minuten auf den Timer).
    
3. Setzen Sie den Computer später 10 Minuten fort.
    
Das Standardverhalten, ohne FIRONOADJUSTMENT, ist, dass Sie warten, bis 4 Minuten für eine Routine noch ausführen. D. h., wurde Zeitgebers angepasst, um zuzulassen, für wie lange der Computer im Standbymodus war. Wenn Sie FIRONOADJUSTMENT übergeben wird jedoch eine Routine im Leerlauf sofort ausgeführt, da Echtzeit von mehr als 5 Minuten verstrichen sind.
  

