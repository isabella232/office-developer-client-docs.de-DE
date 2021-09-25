---
title: DatePart-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Gibt einen numerischen Wert zurück, der den angegebenen Datumsteil des angegebenen Datums darstellt.
ms.openlocfilehash: 4579592a1fbb56d09d87ca396ef12ce94374c3c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569767"
---
# <a name="datepart-function-access-custom-web-app"></a>DatePart-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen numerischen Wert zurück, der den angegebenen Datumsteil des angegebenen Datums darstellt.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DatePart** (*DatePart*, *Date*) 
  
Die **DatePart-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *DatePart*  <br/> |Der Teil von  *Date*  (ein Datums- oder Uhrzeitwert), für den eine ganze Zahl zurückgegeben wird. Eine Liste der gültigen Abkürzungen finden Sie im Abschnitt "Hinweise".  <br/> |
| *Date*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden alle zulässigen  *DatePart*  -Argumente aufgeführt. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**quarter** <br/> |
|**month** <br/> |
|**dayofyear** <br/> |
|**day** <br/> |
|**week** <br/> |
|**Wochentag** <br/> |
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**millisecond** <br/> |
   

