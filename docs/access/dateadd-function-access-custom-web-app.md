---
title: DateAdd-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Addiert zu dem angegebenen Datum die angegebene Anzahl von Intervallen (positive oder negative ganze Zahl) der angegebenen Datumskomponente und gibt das zugehörige Ergebnis zurück.
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282180"
---
# <a name="dateadd-function-access-custom-web-app"></a>DateAdd-Funktion (benutzerdefinierte Access-Web-App)

Addiert zu dem angegebenen Datum die angegebene Anzahl von Intervallen (positive oder negative ganze Zahl) der angegebenen Datumskomponente und gibt das zugehörige Ergebnis zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
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


