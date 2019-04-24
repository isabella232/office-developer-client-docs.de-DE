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
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280054"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Nachrichtendienst-Einstiegspunktfunktion für einen MAPI-Speicheranbieter zum Umschließen eines PST-basierten lokalen Speichers als NST-Speicher. 
  
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

 **NSTServiceEntry** verwendet den Prototyp der **[MSGSERVICEENTRY](msgserviceentry.md)** -Funktion. Informationen zu den Parametern finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Rückgabewerte

Informationen zu Rückgabewerten finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** verwenden, um nach der Adresse dieser Funktion in msmapi32. dll zu suchen, geben Sie "NSTServiceEntry" als Prozedurnamen an. 
  
Um die Replikations-API verwenden zu können, muss ein MAPI-Speicheranbieter zunächst einen PST-basierten lokalen Speicher durch Aufrufen von **[NSTServiceEntry](nstserviceentry.md)** öffnen und einbinden. Der Anbieter kann dann die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)** verwenden, um die Replikation durchzuführen. 
  
Die folgenden Hinweise gelten für einen NST-Speicher:
  
- Speichern Sie keine Informationen im Abschnitt globaler Profil beim Implementieren eines MAPI-Anbieters, der **NSTServiceEntry**verwendet. Der Abschnitt globaler Profil wird von vielen Anbietern gemeinsam genutzt, und in diesem Profil gespeicherte Daten können überschrieben werden. 
    
- Nur Elemente mit vorhandenen Änderungszeit Stempeln erhalten ihre Stempel beim Speichern aktualisiert. 
    
- Die Konfliktüberprüfung tritt nicht automatisch auf, wenn Elemente gespeichert werden.
    
-  Doppelte Erkennung tritt nicht auf, wenn Elemente gespeichert werden. 
    
-  Die Datei, die die zwischengespeicherte Version des Servers darstellt, wird angefügt. NST. 
    
- Wenn Sie einen Zeiger auf den Abschnitt globales Profil erhalten möchten, Ruft ein Nachrichtendienst **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** im Support-Objekt mithilfe von **pbNSTGlobalProfileSectionGuid** wie folgt auf: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- In diesem Fall sollte das Unterstützungsobjekt des Nachrichtendiensts sicherstellen, dass **IMAPISupport:: OpenProfileSection** den Profil Abschnitt zurückgibt, der durch die **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** -Eigenschaft im Standardprofil Abschnitt identifiziert wird. Zum Abrufen dieses Profil Abschnitts kann das Support Objekt den Standardprofil Abschnitt öffnen, **PR_SERVICE_UID**abrufen und das Ergebnis an **IMAPISupport:: OpenProfileSection** zum Abrufen des richtigen globalen Profil Abschnitts weitergeben. Das Support-Objekt gibt wiederum einen Zeiger auf diesen Abschnitt des globalen Profils an den Nachrichtendienst zurück. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)

