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
  
Message service entry point function for a MAPI store provider to wrap a PST-based local store as an NST store. 
  
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

 **NSTServiceEntry verwendet** den **[MSGSERVICEENTRY-Funktionsprototyp.](msgserviceentry.md)** Informationen zu den Parametern finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Rückgabewerte

Informationen zu Rückgabewerten finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie **[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** verwenden, um in msmapi32.dll nach der Adresse dieser Funktion zu suchen, geben Sie "NSTServiceEntry" als Prozedurnamen an. 
  
Um die Replikations-API zu verwenden, muss ein MAPI-Speicheranbieter zunächst einen lokalen PST-basierten Speicher öffnen und umschließen, indem **[er NSTServiceEntry aufruft.](nstserviceentry.md)** Der Anbieter kann dann die Hauptschnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX](ipstxiunknown.md)** verwenden, um die Replikation zu durchführen. 
  
Die folgenden Hinweise gelten für einen NST-Speicher:
  
- Speichern Sie beim Implementieren eines MAPI-Anbieters, der **NSTServiceEntry** verwendet, keine Informationen im Abschnitt globales Profil. Der Abschnitt "Globales Profil" wird von vielen Anbietern freigegeben, und in diesem Profil gespeicherte Daten können überschrieben werden. 
    
- Nur Elemente mit vorhandenen Änderungszeitstempeln erhalten ihre Stempel aktualisiert, wenn sie gespeichert werden. 
    
- Die Konfliktüberprüfung erfolgt nicht automatisch, wenn Elemente gespeichert werden.
    
-  Die Duplikaterkennung erfolgt nicht, wenn Elemente gespeichert werden. 
    
-  Die Datei, die die zwischengespeicherte Version des Servers darstellt, wird mit angefügt. NST. 
    
- Um einen Zeiger auf den globalen Profilabschnitt zu erhalten, ruft ein Nachrichtendienst **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** im Supportobjekt mithilfe von **pbNSTGlobalProfileSectionGuid** auf, wie unten definiert: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- In diesem Fall sollte das Supportobjekt des Nachrichtendiensts sicherstellen, dass **IMAPISupport::OpenProfileSection** den Profilabschnitt zurückgibt, der durch die **[PR_SERVICE_UID-Eigenschaft](pidtagserviceuid-canonical-property.md)** im Standardprofilabschnitt identifiziert wird. Zum Abrufen dieses Profilabschnitts kann das Supportobjekt den Standardprofilabschnitt öffnen, **PR_SERVICE_UID** abrufen und das Ergebnis an **IMAPISupport::OpenProfileSection** übergeben, um den richtigen globalen Profilabschnitt abzurufen. Das Supportobjekt gibt wiederum einen Zeiger auf diesen globalen Profilabschnitt auf den Nachrichtendienst zurück. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)

