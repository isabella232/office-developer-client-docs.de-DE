---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5a632b9ccb31220620ae010dd52b7a147a02c050
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592109"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erhöht die MAPI-Subsystem-Referenzanzahl und initialisiert globale Daten für die MAPI-DLL. 
  
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
  
> [in] Zeiger auf eine [MAPIINIT_0](mapiinit_0.md) Struktur. Der  _parameter lpMapiInit_ kann auf NULL festgelegt werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das MAPI-Subsystem wurde erfolgreich initialisiert.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **MAPIInitialize-Funktion** erhöht die MAPI-Referenzanzahl für das MAPI-Subsystem, und die [MAPIUninitialize-Funktion](mapiuninitialize.md) verringert die Anzahl der internen Verweise. Daher muss die Anzahl der Aufrufe einer Funktion mit der Anzahl der Aufrufe an die andere Funktion übereinstimmen. **MAPIInitialize** gibt S_OK zurück, wenn MAPI noch nicht initialisiert wurde. 
  
Ein Client oder Dienstanbieter muss **MAPIInitialize** aufrufen, bevor ein anderer MAPI-Aufruf erfolgen kann. Andernfalls geben Client- oder Dienstanbieteraufrufe den MAPI_E_NOT_INITIALIZED Wert zurück. 
  
Legen Sie beim Aufrufen von **MAPIInitialize** aus einer Multithreadanwendung den  _Parameter lpMapiInit_ auf eine [MAPIINIT_0](mapiinit_0.md) Struktur fest, die wie folgt deklariert ist: 
  
 **MAPIINIT_0** MAPIINIT= { 0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
und anrufen: 
  
 **MAPIInitialize** ( &amp; MAPIINIT); 
  
Wenn diese Struktur deklariert wird, erstellt MAPI einen separaten Thread zum Behandeln des Benachrichtigungsfensters, das fortgesetzt wird, bis die Initialisierungsreferenzanzahl auf Null fällt. Ein Windows Dienst muss das **Element** MAPIINIT_0 **Struktur,** auf die _lpMapiInit_ verweist, auf MAPI_NT_SERVICE festlegen. 
  
> [!NOTE]
> Sie können **MAPIInitialize** oder **MAPIUninitialize** nicht innerhalb einer Win32 **DllMain-Funktion** oder einer anderen Funktion aufrufen, die Threads erstellt oder beendet. Weitere Informationen finden Sie unter [Using Thread-Safe Objects](using-thread-safe-objects.md). 
  
 **MAPIInitialize** gibt keine erweiterten Fehlerinformationen zurück. Im Gegensatz zu den meisten anderen MAPI-Aufrufen sind die Bedeutungen der Rückgabewerte streng definiert, sodass sie dem jeweiligen Schritt der fehlgeschlagenen Initialisierung entsprechen: 
  
1. Überprüft Parameter und Flags.
    
    MAPI_E_INVALID_PARAMETER oder MAPI_E_UNKNOWN_FLAGS. Der Aufrufer hat einen ungültigen Parameter oder ein ungültiges Kennzeichen übergeben.
    
2. Initialisiert registrierungsschlüssel, die von MAPI erforderlich sind, und bestätigt den Typ des Betriebssystems. Dieser Schritt geschieht nur, wenn der Clientprozess als Dienst unter Windows ausgeführt wird und das MAPI_NT SERVICE-Flag in der **MAPIINIT_0** Struktur festgelegt wird. 
    
    MAPI_E_TOO_COMPLEX. Der aufrufende Prozess ist ein Windows Dienst und Registrierungsschlüssel, die von MAPI benötigt werden, konnten nicht initialisiert werden. 
    
    Weitere Informationen sind möglicherweise im Anwendungsereignisprotokoll verfügbar.
    
3. Überprüfen Sie die Kompatibilität der MAPI mit OLE, und initialisieren Sie OLE.
    
1. Überprüft die Kompatibilität zwischen den aktuellen Versionen von OLE und MAPI. 
    
    MAPI_E_VERSION. Die auf der Arbeitsstation installierte OLE-Version ist nicht mit dieser MapI-Version kompatibel.
    
2. Initialisiert OLE. 
    
    Nur in diesem Schritt kann diese Funktion einen Fehlercode zurückgeben, der hier nicht aufgeführt ist. Es sollte davon ausgegangen werden, dass alle hier  _nicht_ aufgeführten Fehler von der OLE-Funktion **CoInitialize** stammen.
    
4. Initialisiert globale Variablen pro Prozess.
    
    MAPI_E_SESSION_LIMIT. MAPI richtet kontextspezifisch für den aktuellen Prozess ein. Fehler können bei Win16 auftreten, wenn die Anzahl der Prozesse eine bestimmte Anzahl überschreitet, oder auf einem System, wenn der verfügbare Arbeitsspeicher aufgebraucht ist.
    
5. Initialisiert freigegebene globale Variablen aller Prozesse.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Es waren nicht genügend Systemressourcen verfügbar, um den Vorgang abzuschließen.
    
6. Initialisiert das Benachrichtigungsmodul, erstellt sein Fenster und seinen Thread, wenn dies vom flag MAPI_MULTITHREAD_NOTIFICATIONS angefordert wird. 
    
    MAPI_E_INVALID_OBJECT. Kann fehlschlagen, wenn Systemressourcen aufgebraucht sind. 
    
7. Lädt und initialisiert den Profilanbieter. Überprüft, ob **MAPIInitialize** auf den Registrierungsschlüssel zugreifen kann, in dem Profildaten gespeichert sind. 
    
    MAPI_E_NOT_INITIALIZED. Beim Profilanbieter ist ein Fehler aufgetreten. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI verwendet die **MAPIInitialize-Methode,** um die MAPI in einem Hintergrundthread zu initialisieren, um eine Tabellenverarbeitung durchzuführen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

