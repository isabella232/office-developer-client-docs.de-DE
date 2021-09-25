---
title: Format-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Gibt einen Wert zurück, der entsprechend einem bestimmten Muster formatiert ist.
ms.localizationpriority: high
ms.openlocfilehash: 22d56077571405f3b79040cc6739dbd5c77ea405
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568257"
---
# <a name="format-function-access-custom-web-app"></a>Format-Funktion (benutzerdefinierte Access-Web-App)

Gibt einen Wert zurück, der entsprechend einem bestimmten Muster formatiert ist.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: >  *Leider sind Serverprobleme aufgetreten, deshalb können wir \<service\> derzeit nicht hinzufügen. Versuchen Sie es bitte später noch mal.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Format** (*Expression*, *Format*) 
  
Die **Format**-Funktion enthält die folgenden Argumente. 
  
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
    

