---
title: Parse-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analysiert einen Textwert und gibt seinen Wert in einem bestimmten Typ mithilfe der Kultur der Anwendung zurück.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411134"
---
# <a name="parse-function-access-custom-web-app"></a>Parse-Funktion (benutzerdefinierte Access-Web-App)

Analysiert einen Textwert und gibt seinen Wert in einem bestimmten Typ mithilfe der Kultur der Anwendung zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Parse** (*TextExpression*, *DataType*) 
  
Die **Parse-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *TextExpression*  <br/> |Ein Textausdruck, der den formatierten Wert darstellt, der in den angegebenen Datentyp analysiert werden soll.  <br/> |
| *DataType*  <br/> |Literalwert, der den datentyp darstellt, der für das Ergebnis angefordert wurde.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden **Sie Parse** nur zum Konvertieren von Zeichenfolgen in Datums-/Uhrzeit- und Zahlentypen. Verwenden Sie für allgemeine Typkonvertierungen die **Convert-Funktion.** Beachten Sie, dass bei der Analyse des Zeichenfolgenwerts ein bestimmter Leistungsaufwand besteht. 
  

