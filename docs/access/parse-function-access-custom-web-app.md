---
title: Parse-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analysiert einen Textwert und gibt seinen Wert in einem bestimmten Typ mithilfe der Culture der Anwendung zurück.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308057"
---
# <a name="parse-function-access-custom-web-app"></a>Parse-Funktion (Access Custom Web App)

Analysiert einen Textwert und gibt seinen Wert in einem bestimmten Typ mithilfe der Culture der Anwendung zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Analysieren** (*Text*- *Datentyp, DataType*) 
  
Die **Parse** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Text*  <br/> |Ein Textausdruck, der den formatierten Wert darstellt, der in den angegebenen Datentyp analysiert werden soll.  <br/> |
| *DataType*  <br/> |Literalwert, der den für das Ergebnis erforderlichen Datentyp darstellt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie **Parse** nur für die Konvertierung von Zeichenfolge zu Datum/Uhrzeit und Zahlentypen. Verwenden Sie für allgemeine Typkonvertierungen die **Convert** -Funktion. Beachten Sie, dass bei der Analyse des Zeichenfolgenwerts ein bestimmter Leistungsaufwand auftritt. 
  

