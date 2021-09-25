---
title: DateDiff-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Gibt die Anzahl der angegebenen Datumsteilgrenzen zwischen dem angegebenen Start- und Enddatum zurück.
ms.openlocfilehash: 33db2ae5caa55949d0eac86a2bef7f5049d849f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569764"
---
# <a name="datediff-function-access-custom-web-app"></a>DateDiff-Funktion (benutzerdefinierte Access-Web-App)

Gibt die Anzahl der angegebenen Datumsteilgrenzen zwischen dem angegebenen Start- und Enddatum zurück.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateDiff** (*DatePart*, *StartDate*, *EndDate*) 
  
Die **DateDiff-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *DatePart*  <br/> |Ist der Teil von *StartDate* und EndDate, der den Typ der überschrittenen Grenze angibt.  Eine Liste der zulässigen Einstellungen finden Sie im Abschnitt „Hinweise".  <br/> |
| *StartDate*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  <br/> |
| *EndDate*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  <br/> |
   
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
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**millisecond** <br/> |
   

