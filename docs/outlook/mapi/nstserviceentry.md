---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793289"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**Betrifft**: Outlook 
  
Nachricht Service Entry Point-Funktion für MAPI-Speicheranbieter umfließt einen PST-basierten lokalen Speicher als NST Speicher. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Implementiert von:  <br/> |MAPI-Anbieter  <br/> |
|Aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a>Parameter

 **NSTServiceEntry** verwendet den **[MSGSERVICEENTRY](msgserviceentry.md)** Funktionsprototyp. Informationen zu den Parametern finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Rückgabewerte

Informationen zu Rückgabewerte finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Bemerkungen

Wenn **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** für die Adresse des dieser Funktion in msmapi32.dll suchen, geben Sie "NSTServiceEntry" als den Namen der Prozedur. 
  
Um die Replikation-API verwenden, muss ein MAPI-Anbieter zuerst öffnen und in eine PST-basierten lokalen Speicher durch Aufrufen von **[NSTServiceEntry](nstserviceentry.md)** umgebrochen. Der Anbieter können Sie die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)**, um die Replikation auszuführen. 
  
Die folgenden Anmerkungen gelten für einen Speicher NST:
  
- Speichern Sie alle Informationen nicht im Abschnitt globale Profile beim Implementieren von eines MAPI-Anbieters, der die **NSTServiceEntry**verwendet. Abschnitt globale Profile von vielen Anbietern freigegeben und können in diesem Profil gespeicherte Daten überschrieben werden. 
    
- Nur Elemente mit vorhandenen Änderung Zeitstempel erhalten ihre Stempel aktualisiert, wenn sie gespeichert werden. 
    
- Überprüfung von Konflikt tritt nicht automatisch auf Wenn Elemente gespeichert werden.
    
-  Erkennung von Duplikaten tritt nicht auf, wenn Elemente gespeichert werden. 
    
-  Die Datei, die die zwischengespeicherte Version des Servers darstellt angehängt ist. NST. 
    
- Um einen Zeiger auf den Profilabschnitt globale zu ermitteln, ruft eine Message Service **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** im Support-Objekt mit **PbNSTGlobalProfileSectionGuid** wie unten definiert: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- In diesem Fall sollten das Support-Objekt des Diensts Nachricht sicherstellen, dass **IMAPISupport::OpenProfileSection** Profilabschnitt zurückgegeben, der von der **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** -Eigenschaft in den Abschnitt für das Standardprofil identifiziert wird. Wenn in diesem Profilabschnitt erhalten möchten, kann das Support-Objekt öffnen Sie den Abschnitt für das Standardprofil, **PR_SERVICE_UID**abrufen und übergeben Sie das Ergebnis an **IMAPISupport::OpenProfileSection** den richtige globale Profilabschnitt abgerufen. Die Support-Objekts gibt einen Zeiger wiederum für diesen Profilabschnitt globale mit dem Nachrichtendienst. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)

