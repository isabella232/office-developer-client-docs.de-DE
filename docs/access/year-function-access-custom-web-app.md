---
title: Year-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Gibt einen numerischen Wert zurück, der das Jahr des angegebenen Datums im gregorianischen Kalender darstellt.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433122"
---
# <a name="year-function-access-custom-web-app"></a>Year-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen numerischen Wert zurück, der das Jahr des angegebenen Datums im gregorianischen Kalender darstellt.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Year** (*Date*) 
  
Die **Year-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Date*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Von den Funktionen **Year,** **Month** und **Day** zurückgegebene Werte sind gregorianische Werte, unabhängig vom Anzeigeformat für den angegebenen Datumswert. Wenn das Anzeigeformat des angegebenen Datums beispielsweise den Hijri-Kalender verwendet, sind  die zurückgegebenen Werte für die Funktionen **Jahr,** Monat und Tag Werte, die dem entsprechenden gregorianischen Datum zugeordnet sind.  
  

