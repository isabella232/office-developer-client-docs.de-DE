---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280054"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Message Service Entry Points-Funktion für einen MAPI-Speicheranbieter, um einen PST-basierten lokalen Speicher als NST-Speicher einzubinden. 
  
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
  
## <a name="remarks"></a>Hinweise

Wenn Sie **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** verwenden, um nach der Adresse dieser Funktion in msmapi32. dll zu suchen, geben Sie "NSTServiceEntry" als Prozedurnamen an. 
  
Um die Replikations-API verwenden zu können, muss ein MAPI-Speicheranbieter zuerst einen PST-basierten lokalen Speicher öffnen und umbrechen, indem er **[NSTServiceEntry](nstserviceentry.md)** aufruft. Der Anbieter kann dann die Hauptschnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)** verwenden, um die Replikation auszuführen. 
  
Die folgenden Hinweise gelten für einen NST-Speicher:
  
- Speichern Sie beim Implementieren eines MAPI-Anbieters, der **NSTServiceEntry**verwendet, keine Informationen im Abschnitt globales Profil. Der Abschnitt "globaler Profil" wird von vielen Anbietern freigegeben, und die in diesem Profil gespeicherten Daten können überschrieben werden. 
    
- Nur Elemente mit vorhandenen Änderungszeit Stempeln erhalten ihre Stempel aktualisiert, wenn Sie gespeichert werden. 
    
- Die Konfliktprüfung tritt nicht automatisch ein, wenn Elemente gespeichert werden.
    
-  Die doppelte Erkennung tritt nicht auf, wenn Elemente gespeichert werden. 
    
-  Die Datei, die die zwischengespeicherte Version des Servers darstellt, wird angehängt. NST. 
    
- Um einen Zeiger auf den Abschnitt "Global profile" zu erhalten, Ruft ein Nachrichtendienst **[IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md)** im Unterstützungsobjekt mit **pbNSTGlobalProfileSectionGuid** wie unten definiert auf: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- In diesem Fall sollte das Unterstützungsobjekt des Nachrichtendiensts sicherstellen, dass **IMAPISupport:: OpenProfileSection** den Profil Abschnitt zurückgibt, der von der **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** -Eigenschaft im Standardprofil Abschnitt identifiziert wird. Zum Abrufen dieses Profil Abschnitts kann das Support Objekt den Standardprofil Abschnitt öffnen, **PR_SERVICE_UID**abrufen und das Ergebnis an **IMAPISupport:: OpenProfileSection** übergeben, um den richtigen globalen Profil Abschnitt abzurufen. Das Unterstützungsobjekt wiederum gibt einen Zeiger auf diesen globalen Profil Abschnitt zum Nachrichtendienst zurück. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)

