---
title: Format-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Gibt einen Wert nach einem bestimmten Muster formatiert.
ms.openlocfilehash: 1739f87fd6e77c91aa66a64c0b7520fa6a641e95
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387797"
---
# <a name="format-function-access-custom-web-app"></a>Format-Funktion (Access benutzerdefinierte Web app)

Gibt einen Wert nach einem bestimmten Muster formatiert.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Format** (*Ausdruck*, *Format*) 
  
Die **Format** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Expression*  <br/> |Ausdruck, der einen unterstützten Datentyp formatieren.  <br/> |
| *Format*  <br/> | Ein Formatmuster. Das Formatargument muss eine gültige Formatzeichenfolge, entweder als String-Standardformat (z. B. "C" oder "D") oder als ein Muster der benutzerdefinierten Zeichen für Datumsangaben und numerische Werte (beispielsweise "MMMM Dd, Yyyy (Dddd)") enthalten. Weitere Informationen finden Sie unter "Hinweise".  <br/> |
   
## <a name="remarks"></a>Hinweise

Für den *Format* -Parameter können Sie Zeichenfolgen übergeben, die mit einem der folgenden Muster übereinstimmen: 
  
- [Standardmäßige numerische Formatzeichenfolgen](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [Benutzerdefinierte numerische Formatzeichenfolgen](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)
    
- [Formatzeichenfolgen für Datum und Uhrzeit](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)
    
- [Benutzerdefinierte Datums- / Formatieren von Zeichenfolgen](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)
    
Sie können nicht in den folgenden Bereichen von Access 2013 Web apps die **Format** -Funktion verwenden: 
  
- Berechnete Spalten auf Tabellenebene
    
- UI-Makros
    
- Ausdrücke in Ansichten (beispielsweise in Forms)
    

