---
title: Coalesce-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Gibt den ersten Ausdruck zurück, der nicht NULL aus einer Liste von Argumenten ist.
ms.openlocfilehash: e3b238c2aa407a45893cb85ecf3d6867e7f6082f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581707"
---
# <a name="coalesce-function-access-custom-web-app"></a>Coalesce-Funktion (benutzerdefinierte Access-Web-App)

Gibt den ersten Ausdruck zurück, der nicht NULL aus einer Liste von Argumenten ist.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**Coalesce** (*Value*, [*Value*], ...,[*Value*]) 
  
Die **Coalesce-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Wert*  <br/> |Ein Ausdruck.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn alle Argumente NULL sind, gibt **Coalesce** NULL zurück. 
  
## <a name="example"></a>Beispiel

Der folgende Ausdruck wird als Überprüfungsregel für eine Tabelle verwendet. Mit dem Ausdruck wird sichergestellt, dass Einträge in den Feldern "Vorname", "Nachname", "E-Mail", "Mobile Telefon", "Work Telefon", "Home" Telefon und "Company" vorgenommen werden, bevor ein Commit für einen Datensatz ausgeführt wird. Wenn eines der aufgeführten Felder leer gelassen wird, gibt die **Funktion Coalesce** Null zurück, was gegen die Gültigkeitsprüfungsregel verstößt. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


