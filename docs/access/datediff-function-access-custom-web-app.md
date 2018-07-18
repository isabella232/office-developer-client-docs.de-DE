---
title: DateDiff-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Gibt die Anzahl der angegebenen Datum Teil Grenzen zwischen dem angegebenen Startdatum und Enddatum überschritten.
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790215"
---
# <a name="datediff-function-access-custom-web-app"></a>DateDiff-Funktion (Access benutzerdefinierte Web app)

Gibt die Anzahl der angegebenen Datum Teil Grenzen zwischen dem angegebenen Startdatum und Enddatum überschritten.
  
> [!NOTE]
> [!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateDiff** (*DatePart*, *StartDate*, *EndDate*) 
  
Die **DateDiff** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Ist der Teil des *StartDate* und *EndDate* , der den Typ des Grenze überschritten angibt. Eine Liste der zulässigen Einstellungen finden Sie im Abschnitt „Hinweise".  <br/> |
| *StartDate*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  <br/> |
| *EndDate*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  <br/> |
   
## <a name="remarks"></a>Remarks

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
   

