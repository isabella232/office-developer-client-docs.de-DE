---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1fbeccd805953322b579d1490b5e74e5132aa7ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791432"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**Betrifft**: Outlook 
  
Ändert einige oder alle Merkmale eine im Leerlauf Routine [FNIDLE](fnidle.md) basiert. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a>Parameter

_ftg_
  
> [in] Funktion-Tag, die im Leerlauf Routine identifiziert. 
    
_pfnIdle_
  
> [in] Zeiger auf die im Leerlauf Routine. 
    
_pvIdleParam_
  
> [in] Zeiger auf einen neuen Block Arbeitsspeicher, der die aufrufende Implementierung für die im Leerlauf Routine zuweist. 
    
_priIdle_
  
> [in] Wert, der eine neue Priorität für die im Leerlauf Routine darstellt. Mögliche Prioritäten für die Implementierung definierten Routinen sind größer oder kleiner als 0 (null), aber nicht 0 (null). Der Wert 0 (null) ist für eine Benutzerereignis wie klicken mit der Maus oder eine Nachricht WM_PAINT reserviert. Werte, die größer als 0 (null) darstellen Prioritäten für Hintergrund-Vorgänge, die eine höhere Priorität als Veranstaltungen und werden im Rahmen der standardmäßigen Windows-Nachricht Pumpe Schleife verteilt. Werte kleiner als 0 (null) darstellen Prioritäten für im Leerlauf Vorgänge, die nur während der Leerlaufzeit Nachrichtensystem ausgeführt. Beispiele für Prioritäten sind: 1 für die Übermittlung von Vordergrund, für das Einfügen von Power bearbeiten Zeichen 1 und 3 für das Herunterladen von neuer Nachrichten.
    
_csecIdle_
  
> [in] Eine neue Zeit in Hundertstelsekunden, der im Leerlauf Routine zuweisen. Die Bedeutung des ursprünglichen Zeitwerts hängt davon ab, was im _IroIdle_ -Parameter übergeben wird. Es kann sein: 
    
  - Der Mindestzeitraum Untätigkeit für Benutzer, die verstreichen muss, bevor die MAPI ruft im Leerlauf Modul die im Leerlauf Routine zum ersten Mal, wenn das Flag FIROWAIT in _IroIdle_festgelegt ist. Nach der Übergabe diesmal, kann das Modul im Leerlauf die im Leerlauf Routine so oft wie nötig aufrufen. 
    
  - Das kürzeste Intervall zwischen Aufrufen der im Leerlauf Routine, wenn das Flag FIROINTERVAL in _IroIdle_festgelegt ist. 
    
_iroIdle_
  
> [in] Bitmaske aus Flags, die neue Optionen zum Aufrufen der im Leerlauf Routine angibt. Genau einem der folgenden Flags muss festgelegt werden:
    
  - FIROINTERVAL: Die Zeit, die durch den Parameter _CsecIdle_ angegeben ist das kürzeste Intervall zwischen aufeinander folgenden Aufrufen der Routine im Leerlauf. 
      
  - FIROONCEONLY: veraltet. Nicht verwenden. 
      
  - FIROPERBLOCK: veraltet. Nicht verwenden. 
      
  - FIROWAIT: Die Zeit, die durch den Parameter _CsecIdle_ angegeben ist der Mindestzeitraum Untätigkeit für Benutzer, die verstreichen muss, bevor das im Leerlauf MAPI-Modul die im Leerlauf Routine zum ersten Mal aufruft. Nach der Übergabe diesmal, kann das Modul im Leerlauf die im Leerlauf Routine so oft wie nötig aufrufen. 
    
_ircIdle_
  
> [in] Bitmaske der Flags verwendet, um die Änderungen anzugeben, der im Leerlauf Routine vorgenommen werden sollen. Die folgenden Kennzeichen können eine beliebige Kombination festgelegt werden:
    
  - FIRCCSEC: Eine Änderung an den Zeitaufwand für die im Leerlauf Routine, d. h., eine Änderung von der in der _CsecIdle_ -Parameter übergebene Wert angegeben. 
      
  - FIRCIRO: Eine Änderung der Optionen für die Routine im Leerlauf, d. h., eine Änderung angegeben durch den Wert im _IroIdle_ Parameter übergeben. 
      
  - FIRCPFN: Eine Änderung der im Leerlauf routinemäßige Zeiger, d. h., eine Änderung angegeben durch den Wert im _PfnIdle_ Parameter übergeben. 
      
  - FIRCPRI: Eine Änderung der Priorität von der Routine im Leerlauf, d. h., eine Änderung angegeben durch den Wert im _PriIdle_ Parameter übergeben. 
      
  - FIRCPV: Eine Änderung an den Arbeitsspeicher Block mit der Routine im Leerlauf, d. h., eine Änderung angegeben durch den Wert im _PvIdleParam_ Parameter übergeben. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Bemerkungen

Die folgenden Funktionen Umgang mit der MAPI-Modul im Leerlauf und im Leerlauf Routinen basierend auf den [FNIDLE](fnidle.md) Funktionsprototyp: 
  
|**Im Leerlauf routinemäßige-Funktion**|**Verwendung**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Ändert die Eigenschaften einer registrierten im Leerlauf Routine.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Entfernt eine registrierte im Leerlauf Routine aus dem MAPI-System.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Aktiviert oder deaktiviert erneut eine registrierte im Leerlauf Routine ohne aus der MAPI-System entfernt.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Das MAPI-System, mit oder ohne Aktivieren hinzugefügt eine im Leerlauf Routine.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Das im Leerlauf MAPI-Modul für die aufrufende Anwendung geschlossen wird.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialisiert das im Leerlauf MAPI-Modul für die aufrufende Anwendung.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**und **EnableIdleRoutine** werden als Eingabeparameter das Function-Tag von **FtgRegisterIdleRoutine**zurückgegeben. 
  
Wenn alle Vordergrund Aufgaben für die Plattform Leerlauf, ruft das MAPI-im Leerlauf-Modul die höchste Priorität im Leerlauf Routine, die zur Ausführung bereit ist. Es gibt keine Garantie für den Aufruf Reihenfolge zwischen im Leerlauf Routinen, der die gleiche Priorität. 
  

