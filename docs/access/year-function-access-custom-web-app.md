---
title: Year-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Gibt einen numerischen Wert zurück, der das Jahr des angegebenen Datums im gregorianischen Kalender darstellt.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301666"
---
# <a name="year-function-access-custom-web-app"></a>Year-Funktion (Access Custom Web App)

Gibt einen numerischen Wert zurück, der das Jahr des angegebenen Datums im gregorianischen Kalender darstellt.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Jahr** (*Datum*) 
  
Die **year** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Date*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Von den Funktionen **year**, **Month**und **Day** zurückgegebene Werte sind gregorianische Werte, unabhängig vom Anzeigeformat für den angegebenen Datumswert. Wenn beispielsweise im Anzeigeformat des angegebenen Datums der Hijri-Kalender verwendet wird, sind die zurückgegebenen Werte für die Funktionen **year**, **Month**und **Day** Werte, die dem äquivalenten gregorianischen Datum zugeordnet sind. 
  

