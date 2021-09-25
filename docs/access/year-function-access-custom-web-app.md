---
title: Year-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Gibt einen numerischen Wert zurück, der das Jahr des angegebenen Datums im gregorianischen Kalender darstellt.
ms.openlocfilehash: 8eaa7f21b68a92e88c0a7b8f1c01892a416b23a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614633"
---
# <a name="year-function-access-custom-web-app"></a>Year-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen numerischen Wert zurück, der das Jahr des angegebenen Datums im gregorianischen Kalender darstellt.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Jahr** (*Datum*) 
  
Die **Year-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Date*  <br/> |Ein Ausdruck, der in einen Datums-/Uhrzeitwert aufgelöst werden kann. Der  *Date*  -Argumentausdruck, Spaltenausdruck, benutzerdefinierte Variable oder Zeichenfolgenliteral.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die von den Funktionen **"Year",** **"Month"** und **"Day"** zurückgegebenen Werte sind gregorianische Werte, unabhängig vom Anzeigeformat für den angegebenen Datumswert. Wenn beispielsweise das Anzeigeformat des angegebenen Datums den Hijri-Kalender verwendet, sind die zurückgegebenen Werte für die Funktionen **Year**, **Month** und **Day** Werte, die dem entsprechenden gregorianischen Datum zugeordnet sind. 
  

