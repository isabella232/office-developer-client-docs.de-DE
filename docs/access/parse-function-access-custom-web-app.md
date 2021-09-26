---
title: Parse-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analysiert einen Textwert und gibt seinen Wert in einem bestimmten Typ mithilfe der Kultur der Anwendung zurück.
ms.openlocfilehash: e09478cee26accd8e316d3de36d8034f0ca02526
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631538"
---
# <a name="parse-function-access-custom-web-app"></a>Parse-Funktion (benutzerdefinierte Access-Web-App)

Analysiert einen Textwert und gibt seinen Wert in einem bestimmten Typ mithilfe der Kultur der Anwendung zurück.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Parse** (*TextExpression*, *DataType*) 
  
Die **Parse-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *TextExpression*  <br/> |Ein Textausdruck, der den formatierten Wert darstellt, der in den angegebenen Datentyp analysiert werden soll.  <br/> |
| *DataType*  <br/> |Literalwert, der den datentyp darstellt, der für das Ergebnis angefordert wurde.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie **"Parse"** nur zum Konvertieren von Zeichenfolgen- in Datums-/Uhrzeit- und Zahlentypen. Verwenden Sie für allgemeine  Typkonvertierungen die Convert-Funktion. Beachten Sie, dass beim Analysieren des Zeichenfolgenwerts ein bestimmter Leistungsaufwand entsteht. 
  

