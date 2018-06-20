---
title: Parse-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analysiert einen Textwert und gibt den Wert in einem angegebenen Typ unter Verwendung der Kultur der Anwendung zurück.
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790339"
---
# <a name="parse-function-access-custom-web-app"></a>Parse-Funktion (Access benutzerdefinierte Web app)

Analysiert einen Textwert und gibt den Wert in einem angegebenen Typ unter Verwendung der Kultur der Anwendung zurück.
  
> [!NOTE]
> [!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Analysieren** (*TextExpression*, *Datentyp*) 
  
Die **Parse** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Ein Ausdruck, der den formatierten Wert in den angegebenen Datentyp zu analysieren.  <br/> |
| *DataType*  <br/> |Literale Wert, der den Datentyp für das Ergebnis angefordert darstellt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie nur für die Konvertierung von Zeichenfolge Datum/Uhrzeit und Typen der Nummer **zu analysieren** . Verwenden Sie für allgemeine typkonvertierungen die **Convert** -Funktion. Behalten Sie im Hinterkopf, dass es eine bestimmte Leistung führt zu mehr Verarbeitungsaufwand bei der Analyse des String-Werts ist. 
  

