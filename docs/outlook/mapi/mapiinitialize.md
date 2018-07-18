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
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793136"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**Betrifft**: Outlook 
  
Inkrementiert den Referenzzähler des MAPI-Subsystems und globale-Daten für die MAPI-DLL initialisiert. 
  
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
  
> [in] Zeiger auf eine [MAPIINIT_0](mapiinit_0.md) -Struktur. Der Parameter _LpMapiInit_ kann auf NULL festgelegt werden. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> MAPI-Subsystems wurde erfolgreich initialisiert.
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Referenz für das MAPI-Subsystem und die [MAPIUninitialize](mapiuninitialize.md) Funktion dekrementiert zählen **"MAPIInitialize"** Funktion Schritten für die interne verweiszählung. Die Anzahl der Anrufe an eine Funktion muss daher die Anzahl der Aufrufe der anderen entsprechen. **"MAPIInitialize"** gibt S_OK zurück, wenn MAPI zuvor nicht initialisiert wurde. 
  
Ein Client oder Dienstanbieter muss **"MAPIInitialize"** aufrufen, bevor eine beliebige andere MAPI-Aufruf. Dazu wird Client oder Dienst Anbieter Aufrufe den MAPI_E_NOT_INITIALIZED Wert zurückgegeben. 
  
Beim Aufruf von **"MAPIInitialize"** aus einer Multithread-Anwendung, legen Sie den Parameter _LpMapiInit_ auf eine [MAPIINIT_0](mapiinit_0.md) -Struktur, die wie folgt deklariert wird: 
  
 **MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
und rufen Sie: 
  
 **"MAPIInitialize"** (&amp;MAPIINIT); 
  
Wenn diese Struktur deklariert wird, erstellt MAPI einen getrennten Thread, um das Benachrichtigungsfenster verarbeitet werden, wird fortgesetzt, bis der Initialize-Referenzzähler auf 0 (null) fällt aus. Ein Windows-Dienst muss das **Ulflags** Mitglied der **MAPIINIT_0** -Struktur, die auf den _LpMapiInit_ zu MAPI_NT_SERVICE festgelegt. 
  
> [!NOTE]
> **"MAPIInitialize"** oder **MAPIUninitialize** aus kann nicht innerhalb einer Win32 **DllMain** -Funktion oder eine andere Funktion, die erstellt oder Threads beendet aufgerufen werden. Weitere Informationen finden Sie unter [Verwenden von threadsicheren Objekten](using-thread-safe-objects.md). 
  
 **"MAPIInitialize"** gibt keine erweiterten Fehlerinformationen zurück. Im Gegensatz zu den meisten anderen MAPI-Aufrufe sind die Bedeutung der seine Rückgabewerte streng, um mit dem bestimmten Schritt der Initialisierung entsprechen, die nicht definiert: 
  
1. Überprüft, Parameter und Kennzeichen.
    
    MAPI_E_INVALID_PARAMETER oder MAPI_E_UNKNOWN_FLAGS. Ungültiger Parameter oder Flag Aufrufer übergeben werden.
    
2. Initialisiert MAPI erforderliche Registrierungsschlüssel, und die Art des Betriebssystems bestätigt. Dieser Schritt tritt nur auf, wenn der Clientprozess als Dienst unter Windows ausgeführt wird und das Flag MAPI_NT-Dienst in der Struktur **MAPIINIT_0** festgelegt. 
    
    MAPI_E_TOO_COMPLEX. Der aufrufende Prozess ist ein Windows-Dienst und MAPI erforderliche Registrierungsschlüssel konnte nicht initialisiert werden. 
    
    Zusätzliche Informationen möglicherweise im Anwendungsereignisprotokoll zur Verfügung.
    
3. Überprüfen Sie die Kompatibilität von MAPI mit OLE und anschließend werden Sie OLE initialisiert.
    
1. Überprüft die Kompatibilität zwischen den aktuellen Versionen von OLE und MAPI. 
    
    MAPI_E_VERSION. Auf der Arbeitsstation installierte OLE-Version ist nicht kompatibel mit dieser Version von MAPI.
    
2. OLE initialisiert. 
    
    In diesem Schritt nur kann diese Funktion nicht aufgelisteten Fehlercode zurück. Etwaige Fehler _nicht_ aufgeführt Hier sollte angenommen werden, dass der OLE-Funktion **CoInitialize**stammen.
    
4. Initialisiert pro Prozess globale Variablen.
    
    MAPI_E_SESSION_LIMIT. MAPI richtet Kontext speziell für den aktuellen Prozess. Fehler können auftreten, Win16 übersteigt die Anzahl der Prozesse eine bestimmte Anzahl oder auf einem System verfügbaren Arbeitsspeicher ausgeschöpft ist.
    
5. Initialisiert gemeinsam genutzte globale Variablen von allen Prozessen.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Nicht genügend Systemressourcen waren zum Abschließen des Vorgangs verfügbar.
    
6. Initialisiert das Modul Benachrichtigung, die zugehörigen Fenster und einem Thread erstellt, wenn durch das Flag MAPI_MULTITHREAD_NOTIFICATIONS angefordert. 
    
    MAPI_E_INVALID_OBJECT. Kann fehlschlagen Systemressourcen aufgebraucht sind. 
    
7. Lädt und initialisiert den Benutzerprofildienst-Anbieter. Stellt sicher, dass **"MAPIInitialize"** den Registrierungsschlüssel zugreifen können, auf dem Profildaten gespeichert sind. 
    
    MAPI_E_NOT_INITIALIZED. Der Benutzerprofildienst-Anbieter ist ein Fehler aufgetreten. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI (engl.) verwendet die Methode **"MAPIInitialize"** MAPI in einem Hintergrundthread die einige Tabelle Verarbeitung nicht initialisiert werden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

