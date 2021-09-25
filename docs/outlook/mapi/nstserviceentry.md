---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d68efa728b2cd62aca4ffbce02d2ea894ff74c35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595637"
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

 **NSTServiceEntry** verwendet den Prototyp der **[MSGSERVICEENTRY-Funktion.](msgserviceentry.md)** Informationen zu den Parametern finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Rückgabewerte

Informationen zu Rückgabewerten finden Sie unter **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn **[Sie GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)** zum Suchen nach der Adresse dieser Funktion in msmapi32.dll verwenden, geben Sie "NSTServiceEntry" als Prozedurnamen an. 
  
Um die Replikations-API zu verwenden, muss ein MAPI-Speicheranbieter zuerst einen PST-basierten lokalen Speicher öffnen und umschließen, indem **[er NSTServiceEntry aufruft.](nstserviceentry.md)** Der Anbieter kann dann die wichtigsten Schnittstellen der API, **[IOSTX](iostxiunknown.md)** und **[IPSTX,](ipstxiunknown.md)** verwenden, um die Replikation durchzuführen. 
  
Die folgenden Hinweise gelten für einen NST-Speicher:
  
- Speichern Sie keine Informationen im globalen Profilabschnitt, wenn Sie einen MAPI-Anbieter implementieren, der **NSTServiceEntry** verwendet. Der globale Profilabschnitt wird von vielen Anbietern gemeinsam genutzt, und in diesem Profil gespeicherte Daten können überschrieben werden. 
    
- Nur Elemente mit vorhandenen Änderungszeitstempeln werden beim Speichern aktualisiert. 
    
- Die Konfliktüberprüfung erfolgt nicht automatisch, wenn Elemente gespeichert werden.
    
-  Beim Speichern von Elementen tritt keine Duplikaterkennung auf. 
    
-  Die Datei, die die zwischengespeicherte Version des Servers darstellt, wird mit angefügt. NST. 
    
- Um einen Zeiger auf den globalen Profilabschnitt abzurufen, ruft ein Nachrichtendienst **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** im Supportobjekt mit **pbNSTGlobalProfileSectionGuid** auf, wie unten definiert: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- In diesem Fall sollte das Supportobjekt des Nachrichtendiensts sicherstellen, dass **IMAPISupport::OpenProfileSection** den Profilabschnitt zurückgibt, der von der **[PR_SERVICE_UID-Eigenschaft](pidtagserviceuid-canonical-property.md)** im Standardprofilabschnitt identifiziert wird. Um diesen Profilabschnitt abzurufen, kann das Supportobjekt den Standardprofilabschnitt öffnen, **PR_SERVICE_UID** abrufen und das Ergebnis an **IMAPISupport::OpenProfileSection** übergeben, um den richtigen globalen Profilabschnitt abzurufen. Das Supportobjekt gibt wiederum einen Zeiger auf diesen globalen Profilabschnitt an den Nachrichtendienst zurück. 
    
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)

