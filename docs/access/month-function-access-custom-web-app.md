---
title: Month-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Gibt eine ganze Zahl zurück, die den Monat des angegebenen Datums darstellt.
ms.openlocfilehash: cd3cc1b58b70c0770aa578e8172e23e2718fa272
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576835"
---
# <a name="month-function-access-custom-web-app"></a>Month-Funktion (benutzerdefinierte Access-Web-App)

Gibt eine ganze Zahl zurück, die den Monat des angegebenen Datums darstellt.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Month** (*Date*) 
  
Die **Month-Funktion** enthält das folgende Argument. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Date*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 **Month** gibt den gleichen Wert wie **DatePart** (Monat, Datum) zurück. 
  
Wenn  *Date*  nur einen Zeitteil enthält, ist der Rückgabewert 1, der Basismonat. 
  

