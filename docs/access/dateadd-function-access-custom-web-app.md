---
title: DateAdd-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Addiert zu dem angegebenen Datum die angegebene Anzahl von Intervallen (positive oder negative ganze Zahl) der angegebenen Datumskomponente und gibt das zugehörige Ergebnis zurück.
ms.openlocfilehash: 1719a69859515287357effb6e8a2bed153e51717
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586467"
---
# <a name="dateadd-function-access-custom-web-app"></a>DateAdd-Funktion (benutzerdefinierte Access-Web-App)

Addiert zu dem angegebenen Datum die angegebene Anzahl von Intervallen (positive oder negative ganze Zahl) der angegebenen Datumskomponente und gibt das zugehörige Ergebnis zurück.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateAdd** (*DatePart*, *Number*, *Date*) 
  
Die **DateAdd**-Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *DatePart*  <br/> |Die  *Date*  -Komponente, zu der eine ganze Zahl addiert wird. Eine Liste der zulässigen Einstellungen finden Sie im Abschnitt „Hinweise".  <br/> |
| *Number*  <br/> |Ist ein Ausdruck, der in eine ganze Zahl aufgelöst werden kann, die zu der  *DatePart*  -Komponente von  *Date*  addiert wird. Wenn Sie einen Wert mit einem Dezimalbruch angeben, wird der Bruch gekürzt.  <br/> |
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
|**hour** <br/> |
|**minute** <br/> |
|**second** <br/> |
|**millisecond** <br/> |
   
## <a name="example"></a>Beispiel

Mit dem folgenden Ausdruck wird der letzte Tag des Monats berechnet.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

Mit dem folgenden Ausdruck wird der letzte Tag des vorherigen Monats berechnet.
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


