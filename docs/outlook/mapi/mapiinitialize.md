---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346641"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Inkrementiert den Verweiszähler für das MAPI-Subsystem und initialisiert globale Daten für die MAPI-DLL. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Parameter

 _lpMapiInit_
  
> in Zeiger auf eine [MAPIINIT_0](mapiinit_0.md) -Struktur. Der _lpMapiInit_ -Parameter kann auf NULL festgelegt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das MAPI-Subsystem wurde erfolgreich initialisiert.
    
## <a name="remarks"></a>Bemerkungen

Die **MAPIInitialize** -Funktion erhöht die MAPI-Verweisanzahl für das MAPI-Subsystem, und die [MAPIUninitialize](mapiuninitialize.md) -Funktion dekrementiert den internen Verweiszähler. Daher muss die Anzahl der Aufrufe an eine Funktion der Anzahl der Aufrufe der anderen entsprechen. **MAPIInitialize** gibt S_OK zurück, wenn MAPI nicht zuvor initialisiert wurde. 
  
Ein Client oder ein Dienstanbieter muss **MAPIInitialize** aufrufen, bevor ein anderer MAPI-Aufruf vorgenommen wird. Wenn dies nicht der Fall ist, werden Client-oder Dienstanbieter Aufrufe zum Zurückgeben des MAPI_E_NOT_INITIALIZED-Werts veranlasst. 
  
Wenn Sie **MAPIInitialize** von einer Multithread-Anwendung aufrufen, legen Sie den Parameter _LpMapiInit_ auf eine [MAPIINIT_0](mapiinit_0.md) -Struktur fest, die wie folgt deklariert wird: 
  
 **MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
und rufen Sie an: 
  
 **MAPIInitialize** (&amp;MAPIINIT); 
  
Wenn diese Struktur deklariert wird, erstellt MAPI einen separaten Thread zur Behandlung des Benachrichtigungsfensters, das fortgesetzt wird, bis der Initialisierungs Verweiszähler auf Null fällt. Ein Windows-Dienst muss das **ulflags** -Element der **MAPIINIT_0** -Struktur festlegen, auf die von _lpMapiInit_ auf MAPI_NT_SERVICE verwiesen wird. 
  
> [!NOTE]
> Sie können **MAPIInitialize** oder **MAPIUninitialize** nicht über eine Win32- **DllMain** -Funktion oder eine andere Funktion aufrufen, die Threads erstellt oder beendet. Weitere Informationen finden Sie unter [Verwenden von Thread sicheren Objekten](using-thread-safe-objects.md). 
  
 **MAPIInitialize** gibt keine erweiterten Fehlerinformationen zurück. Im Gegensatz zu den meisten anderen MAPI-aufrufen werden die Bedeutungen der Rückgabewerte strikt definiert, um dem fehlerhaften Schritt der Initialisierung zu entsprechen: 
  
1. Überprüft Parameter und Flags.
    
    MAPI_E_INVALID_PARAMETER oder MAPI_E_UNKNOWN_FLAGS. Der Aufrufer hat den ungültigen Parameter oder das Flag übergeben.
    
2. Initialisiert die für MAPI erforderlichen Registrierungsschlüssel und bestätigt den Betriebssystemtyp. Dieser Schritt tritt nur auf, wenn der Clientprozess unter Windows als Dienst ausgeführt wird und das MAPI_NT-Dienst Kennzeichen in der **MAPIINIT_0** -Struktur festlegt. 
    
    MAPI_E_TOO_COMPLEX. Der aufrufende Prozess ist ein Windows-Dienst, und Registrierungsschlüssel, die für MAPI erforderlich sind, konnten nicht initialisiert werden. 
    
    Möglicherweise stehen im Anwendungsereignisprotokoll zusätzliche Informationen zur Verfügung.
    
3. Überprüfen Sie, ob MAPI mit OLE kompatibel ist, und initialisieren Sie dann OLE.
    
1. Überprüft die Kompatibilität zwischen den aktuellen Versionen von OLE und MAPI. 
    
    MAPI_E_VERSION. Die auf der Arbeitsstation installierte OLE-Version ist mit dieser Version von MAPI nicht kompatibel.
    
2. Initialisiert OLE. 
    
    Während dieses Schritts kann diese Funktion einen Fehlercode zurückgeben, der hier nicht aufgeführt wird. Jeder Fehler, der hier _nicht_ aufgeführt wird, sollte davon ausgehen, dass er von der OLE-Funktion " **Initialize**" stammt.
    
4. Initialisiert globale Variablen pro Prozess.
    
    MAPI_E_SESSION_LIMIT. MAPI richtet kontextspezifisch für den aktuellen Prozess ein. Fehler können auf Win16 auftreten, wenn die Anzahl der Prozesse eine bestimmte Zahl überschreitet oder wenn der verfügbare Arbeitsspeicher erschöpft ist.
    
5. Initialisiert gemeinsame globale Variablen aller Prozesse.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Es waren nicht genügend Systemressourcen verfügbar, um den Vorgang abzuschließen.
    
6. Initialisiert das Benachrichtigungsmodul, erstellt sein Fenster und seinen Thread, wenn es vom MAPI_MULTITHREAD_NOTIFICATIONS-Flag angefordert wird. 
    
    MAPI_E_INVALID_OBJECT. Kann fehlschlagen, wenn Systemressourcen erschöpft sind. 
    
7. Lädt und initialisiert den Profilanbieter. Überprüft, ob **MAPIInitialize** auf den Registrierungsschlüssel zugreifen kann, in dem die Profildaten gespeichert werden. 
    
    MAPI_E_NOT_INITIALIZED. Der Profilanbieter hat einen Fehler festgestellt. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> ||MFCMAPI verwendet die **MAPIInitialize** -Methode, um MAPI in einem Hintergrundthread für die Verarbeitung bestimmter Tabellen zu initialisieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

