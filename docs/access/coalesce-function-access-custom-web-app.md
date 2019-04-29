---
title: ZusammenFügungsfunktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Gibt den ersten Ausdruck, der nicht NULL ist, aus einer Liste von Argumenten zurück.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411393"
---
# <a name="coalesce-function-access-custom-web-app"></a>ZusammenFügungsfunktion (Access Custom Web App)

Gibt den ersten Ausdruck, der nicht NULL ist, aus einer Liste von Argumenten zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**Verschmelzen** (*Wert*, [*Wert*],..., [*Wert*]) 
  
Die **verschmelzen** -Funktion enthält die folgenden Argumente 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Wert*  <br/> |Ein Ausdruck.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn alle Argumente NULL sind, **** gibt verschmelzen NULL zurück. 
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck wird als Gültigkeitsprüfungsregel für eine Tabelle verwendet. Der Ausdruck stellt sicher, dass die Einträge in den Feldern vorName, Nachname, E-Mail, Mobiltelefon, Telefon, privat Telefon und Unternehmen vorgenommen werden, bevor ein Commit ausgeführt wird. Wenn eines der aufgelisteten Felder leer bleibt, gibt **** die Zusammenführungsfunktion NULL zurück, die gegen die Validierungsregel verstößt. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


