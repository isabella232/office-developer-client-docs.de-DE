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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6464f16d9ad73b332ff20dc007ef162b9525c6d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411176"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erhöht die Referenzanzahl des MAPI-Subsystems und initialisiert globale Daten für die MAPI-DLL. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Parameter

 _lpMapiInit_
  
> [in] Zeiger auf [eine MAPIINIT_0](mapiinit_0.md) Struktur. Der  _lpMapiInit-Parameter_ kann auf NULL festgelegt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das MAPI-Subsystem wurde erfolgreich initialisiert.
    
## <a name="remarks"></a>Hinweise

Die **MAPIInitialize-Funktion** erhöht die MAPI-Referenzanzahl für das MAPI-Subsystem, und die [MAPIUninitialize-Funktion](mapiuninitialize.md) dekrementiert die interne Referenzanzahl. Daher muss die Anzahl der Aufrufe einer Funktion der Anzahl der Aufrufe an die andere entspricht. **MAPIInitialize** gibt S_OK zurück, wenn MAPI noch nicht initialisiert wurde. 
  
Ein Client oder Dienstanbieter muss **MAPIInitialize aufrufen,** bevor ein anderer MAPI-Aufruf ausgeführt wird. Anderndienst führt dazu, dass Client- oder Dienstanbieteraufrufe den wert MAPI_E_NOT_INITIALIZED zurückgeben. 
  
Wenn Sie **MAPIInitialize** aus einer Multithreadanwendung aufrufen, legen Sie den  _lpMapiInit-Parameter_ auf eine MAPIINIT_0 [fest,](mapiinit_0.md) die wie folgt deklariert wird: 
  
 **MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
und rufen Sie an: 
  
 **MAPIInitialize** ( &amp; MAPIINIT); 
  
Wenn diese Struktur deklariert wird, erstellt MAPI einen separaten Thread für die Verarbeitung des Benachrichtigungsfensters, der fortgesetzt wird, bis die Initialisierungsreferenzanzahl auf Null fällt. Ein Windows-Dienst muss das **ulflags-Element** der MAPIINIT_0, auf die _von lpMapiInit_ verwiesen wird, auf MAPI_NT_SERVICE.  
  
> [!NOTE]
> Sie können **MAPIInitialize** oder **MAPIUninitialize** nicht innerhalb einer Win32 **DllMain-Funktion** oder einer anderen Funktion aufrufen, die Threads erstellt oder beendet. Weitere Informationen finden Sie unter [Using Thread-Safe Objects](using-thread-safe-objects.md). 
  
 **MAPIInitialize** gibt keine erweiterten Fehlerinformationen zurück. Im Gegensatz zu den meisten anderen MAPI-Aufrufen sind die Bedeutungen der Rückgabewerte genau so definiert, dass sie dem jeweiligen Schritt der initialisierung entsprechen, der fehlgeschlagen ist: 
  
1. Überprüft Parameter und Kennzeichen.
    
    MAPI_E_INVALID_PARAMETER oder MAPI_E_UNKNOWN_FLAGS. Der Aufrufer hat ungültige Parameter oder Kennzeichen übergeben.
    
2. Initialisiert die von MAPI erforderlichen Registrierungsschlüssel und bestätigt den Betriebssystemtyp. Dieser Schritt erfolgt nur, wenn der Clientprozess als Dienst unter Windows ausgeführt wird und das MAPI_NT SERVICE-Flag in der MAPIINIT_0 **legt.** 
    
    MAPI_E_TOO_COMPLEX. Der Aufrufprozess ist ein Windows, und die von MAPI erforderlichen Registrierungsschlüssel konnten nicht initialisiert werden. 
    
    Im Anwendungsereignisprotokoll sind möglicherweise weitere Informationen verfügbar.
    
3. Überprüfen Sie die Kompatibilität von MAPI mit OLE, und initialisieren Sie OLE.
    
1. Überprüft die Kompatibilität zwischen den aktuellen Versionen von OLE und MAPI. 
    
    MAPI_E_VERSION. Die auf der Arbeitsstation installierte Version von OLE ist nicht mit dieser Version von MAPI kompatibel.
    
2. Initialisiert OLE. 
    
    Nur während dieses Schritts kann diese Funktion einen Fehlercode zurückgeben, der hier nicht aufgeführt ist. Alle hier _nicht_ aufgeführten Fehler sollten von der OLE-Funktion **CoInitialize stammen.**
    
4. Initialisiert globale Variablen pro Prozess.
    
    MAPI_E_SESSION_LIMIT. MAPI richtet kontextspezifisch für den aktuellen Prozess ein. Fehler können bei Win16 auftreten, wenn die Anzahl der Prozesse eine bestimmte Anzahl überschreitet, oder auf einem beliebigen System, wenn der verfügbare Arbeitsspeicher ausgeschöpft ist.
    
5. Initialisiert freigegebene globale Variablen aller Prozesse.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Es waren nicht genügend Systemressourcen verfügbar, um den Vorgang abschließen zu können.
    
6. Initialisiert das Benachrichtigungsmodul, erstellt sein Fenster und seinen Thread, wenn es vom Flag MAPI_MULTITHREAD_NOTIFICATIONS wird. 
    
    MAPI_E_INVALID_OBJECT. Kann fehlschlagen, wenn die Systemressourcen ausgeschöpft sind. 
    
7. Lädt und initialisiert den Profilanbieter. Überprüft, ob **MAPIInitialize** auf den Registrierungsschlüssel zugreifen kann, in dem Profildaten gespeichert werden. 
    
    MAPI_E_NOT_INITIALIZED. Beim Profilanbieter ist ein Fehler aufgetreten. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI verwendet die **MAPIInitialize-Methode,** um MAPI in einem Hintergrundthread zu initialisieren, um einige Tabellenverarbeitungen zu machen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

