---
title: Update-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Gibt zurück, ob ein INSERT- oder UPDATE-Vorgang für das angegebene Feld versucht wurde.
ms.openlocfilehash: 0ec2576a95c76be2f61abbd59c7de098a160c279
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614647"
---
# <a name="update-function-access-custom-web-app"></a>Update-Funktion (benutzerdefinierte Access-Web-App)

Gibt zurück, ob ein INSERT- oder UPDATE-Vorgang für das angegebene Feld versucht wurde.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Update** (*Spalte*) 
  
Die **Update-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Column*  <br/> |Der Name des Felds, das auf einen INSERT- oder UPDATE-Vorgang überprüft werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **Update-Funktion** gibt TRUE zurück, unabhängig davon, ob ein INSERT- oder UPDATE-Versuch erfolgreich ist. 
  

