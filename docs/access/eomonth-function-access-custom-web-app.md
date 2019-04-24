---
title: EOMonth-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Gibt den letzten Tag des Monats vor oder angegebene Anzahl von Monaten zurück.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302560"
---
# <a name="eomonth-function-access-custom-web-app"></a>EOMonth-Funktion (Access Custom Web App)

Gibt den letzten Tag des Monats vor oder angegebene Anzahl von Monaten zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **EOMonth** (*Datum*, *NumberOfMonth*) 
  
Die **EOMonth** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Date*  <br/> |Das Startdatum im Datum/Uhrzeit-Format oder in einer akzeptierten Textdarstellung eines Datums.  <br/> |
| *NumberOfMonth*  <br/> |Eine Zahl, die die Anzahl der Monate vor oder nach dem *Datum* darstellt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn *Date* kein gültiges Datum ist, gibt **EOMonth** einen Fehler zurück. 
  
Wenn *Date* Plus *NumberOfMonth* ein ungültiges Datum ergibt, gibt **EOMonth** einen Fehler zurück. 
  

