---
title: Format-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Gibt einen Wert nach einem bestimmten Muster formatiert.
ms.openlocfilehash: 974b56ab8e6bc3f97c1931ba67ca9cd08c3511c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790222"
---
# <a name="format-function-access-custom-web-app"></a>Format-Funktion (Access benutzerdefinierte Web app)

Gibt einen Wert nach einem bestimmten Muster formatiert.
  
> [!NOTE]
> [!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Format** (*Ausdruck*, *Format*) 
  
Die **Format** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Expression*  <br/> |Ausdruck, der einen unterstützten Datentyp formatieren.  <br/> |
| *Format*  <br/> | Ein Formatmuster. Das Formatargument muss eine gültige Formatzeichenfolge, entweder als String-Standardformat (z. B. "C" oder "D") oder als ein Muster der benutzerdefinierten Zeichen für Datumsangaben und numerische Werte (beispielsweise "MMMM Dd, Yyyy (Dddd)") enthalten. Weitere Informationen finden Sie unter "Hinweise".  <br/> |
   
## <a name="remarks"></a>Hinweise

Für den *Format* -Parameter können Sie Zeichenfolgen übergeben, die mit einem der folgenden Muster übereinstimmen: 
  
- [Standardmäßige numerische Formatzeichenfolgen](http://msdn.microsoft.com/en-us/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [Benutzerdefinierte numerische Formatzeichenfolgen](http://msdn.microsoft.com/en-us/library/0c899ak8%28v=vs.110%29.aspx)
    
- [Formatzeichenfolgen für Datum und Uhrzeit](http://msdn.microsoft.com/en-us/library/az4se3k1%28v=vs.110%29.aspx)
    
- [Benutzerdefinierte Datums- / Formatieren von Zeichenfolgen](http://msdn.microsoft.com/en-us/library/8kb3ddd4%28v=vs.110%29.aspx)
    
Sie können nicht in den folgenden Bereichen von Access 2013 Web apps die **Format** -Funktion verwenden: 
  
- Berechnete Spalten auf Tabellenebene
    
- UI-Makros
    
- Ausdrücke in Ansichten (beispielsweise in Forms)
    

