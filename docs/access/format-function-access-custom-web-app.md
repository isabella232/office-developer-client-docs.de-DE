---
title: Format-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Gibt einen Wert zurück, der entsprechend einem bestimmten Muster formatiert ist.
localization_priority: Priority
ms.openlocfilehash: 5331df30f276a7edd0571e9bf24c759d57ec6a54
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710391"
---
# <a name="format-function-access-custom-web-app"></a>Format-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen Wert zurück, der entsprechend einem bestimmten Muster formatiert ist.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Format** (*Expression*, *Format*) 
  
Die **Format **-Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Ausdruck*  <br/> |Ausdruck eines unterstützten Datentyps, der formatiert werden soll.  <br/> |
| *Format*  <br/> | Ein Formatmuster. Das Formatargument muss eine gültige Formatzeichenfolge enthalten, entweder als Standardformatzeichenfolge (z. B. „C“ oder „D“), oder als Muster von benutzerdefinierten Zeichen für Datumsangaben und numerische Werte (z. B. „MMM dd, yyyy (dddd)“). Weitere Informationen hierzu finden Sie unter „Hinweise“.  <br/> |
   
## <a name="remarks"></a>Hinweise

Für den *Format*-Parameter können Sie Zeichenfolgen übergeben, die einem der folgenden Muster entsprechen: 
  
- [Standardmäßige Formatzeichenfolgen für numerische Werte](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [Benutzerdefinierte Formatzeichenfolgen für numerische Werte](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)
    
- [Standardmäßige Formatzeichenfolgen für Datums- und Uhrzeitangaben](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)
    
- [Benutzerdefinierte Formatzeichenfolgen für Datums- und Uhrzeitangaben](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)
    
In den folgenden Bereichen der Access 2013-Web-Apps können Sie die **Format**-Funktion nicht verwenden: 
  
- Berechnete Spalten auf Tabellenebene
    
- Benutzeroberflächenmakros
    
- Ausdrücke in Ansichten (z. B. in Formularen)
    

