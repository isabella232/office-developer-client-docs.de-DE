---
title: Try_Parse-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analysiert einen Textwert auf den angegebenen Datentyp in der Kultur der Anwendung oder gibt Null zurück, wenn die Konvertierung ungültig ist.
ms.openlocfilehash: ee4007dee0b000f8093c61a095df91a4dd56fc66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588406"
---
# <a name="try_parse-function-access-custom-web-app"></a>Try_Parse-Funktion (benutzerdefinierte Access-Web-App)

Analysiert einen Textwert auf den angegebenen Datentyp in der Kultur der Anwendung oder gibt Null zurück, wenn die Konvertierung ungültig ist.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Try_Parse** (*TextExpression*, *DataType*) 
  
Die **Try_Parse-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *TextExpression*  <br/> |Ein Textausdruck, der den formatierten Wert darstellt, der in den angegebenen Datentyp analysiert werden soll.  <br/> |
| *DataType*  <br/> |Der Datentyp, in den  *TextExpression*  analysiert werden soll.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie **Try_Parse** nur für die Konvertierung von Zeichenfolgen in Datums-/Uhrzeit- und Zahlentypen. Verwenden Sie für allgemeine Typkonvertierungen weiterhin **Convert**. 
  

