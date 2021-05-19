---
title: Try_Parse-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analysiert einen Textwert für den angegebenen Datentyp in der Kultur der Anwendung oder gibt Null zurück, wenn die Konvertierung ungültig ist.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427528"
---
# <a name="try_parse-function-access-custom-web-app"></a>Try_Parse-Funktion (benutzerdefinierte Access-Web-App)

Analysiert einen Textwert für den angegebenen Datentyp in der Kultur der Anwendung oder gibt Null zurück, wenn die Konvertierung ungültig ist.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Try_Parse** (*TextExpression*, *DataType*) 
  
Die **Try_Parse** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *TextExpression*  <br/> |Ein Textausdruck, der den formatierten Wert darstellt, der in den angegebenen Datentyp analysiert werden soll.  <br/> |
| *DataType*  <br/> |Der Datentyp, in den *TextExpression analysiert werden soll.*  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden **Try_Parse** nur zum Konvertieren von Zeichenfolgen in Datums-/Uhrzeit- und Zahlentypen. Verwenden Sie für allgemeine Typkonvertierungen weiterhin **Convert**. 
  

