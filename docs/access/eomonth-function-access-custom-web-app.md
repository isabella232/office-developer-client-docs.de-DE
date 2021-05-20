---
title: EOMonth-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Gibt den letzten Tag des Monats vor oder die angegebene Anzahl von Monaten zurück.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437455"
---
# <a name="eomonth-function-access-custom-web-app"></a>EOMonth-Funktion (benutzerdefinierte Access-Web-App)

Gibt den letzten Tag des Monats vor oder die angegebene Anzahl von Monaten zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **EOMonth** (*Date*, *NumberOfMonth*) 
  
**EOMonth** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Date*  <br/> |Das Startdatum im Datums-/Uhrzeitformat oder in einer akzeptierten Textdarstellung eines Datums.  <br/> |
| *NumberOfMonth*  <br/> |Eine Zahl, die die Anzahl der Monate vor oder nach dem *Datum darstellt.*  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn  *Date*  kein gültiges Datum ist, **gibt EOMonth** einen Fehler zurück. 
  
Wenn  *Date*  plus  *NumberOfMonth*  ein ungültiges Datum ergibt, gibt **EOMonth** einen Fehler zurück. 
  

