---
title: Try_Parse-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analysiert ein Textwerts in den angegebenen Datentyp in der Kultur der Anwendung, oder gibt Null zurück, wenn die Konvertierung nicht gültig ist.
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790379"
---
# <a name="tryparse-function-access-custom-web-app"></a>Try_Parse-Funktion (Access benutzerdefinierte Web app)

Analysiert ein Textwerts in den angegebenen Datentyp in der Kultur der Anwendung, oder gibt Null zurück, wenn die Konvertierung nicht gültig ist.
  
> [!NOTE]
> [!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Try_Parse** (*TextExpression*, *Datentyp*) 
  
Die **Try_Parse** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Ein Ausdruck, der den formatierten Wert in den angegebenen Datentyp zu analysieren.  <br/> |
| *DataType*  <br/> |Der Datentyp in die *TextExpression* zu analysieren.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie **Try_Parse** nur für die Konvertierung von Zeichenfolge Datum/Uhrzeit und Typen der Nummer. Allgemeine typkonvertierungen auch weiterhin **Konvertieren**verwenden. 
  

