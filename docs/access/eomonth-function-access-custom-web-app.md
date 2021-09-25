---
title: EOMonth-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Gibt den letzten Tag des Monats vor oder die angegebene Anzahl von Monaten zurück.
ms.openlocfilehash: 6330865fa904fe2011d3cfaab988214950df51b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601569"
---
# <a name="eomonth-function-access-custom-web-app"></a>EOMonth-Funktion (benutzerdefinierte Access-Web-App)

Gibt den letzten Tag des Monats vor oder die angegebene Anzahl von Monaten zurück.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **EOMonth** (*Date*, *NumberOfMonth*) 
  
Der **EOMonth** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Date*  <br/> |Das Startdatum im Datums-/Uhrzeitformat oder in einer akzeptierten Textdarstellung eines Datums.  <br/> |
| *NumberOfMonth*  <br/> |Eine Zahl, die die Anzahl der Monate vor oder nach dem  *Datum*  darstellt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn  *Date*  kein gültiges Datum ist, gibt **EOMonth** einen Fehler zurück. 
  
Wenn  *Date*  plus  *NumberOfMonth*  ein ungültiges Datum ergibt, gibt **EOMonth** einen Fehler zurück. 
  

