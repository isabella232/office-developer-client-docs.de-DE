---
title: Update-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Gibt zurück, ob ein Einfüge-oder Aktualisierungsvorgang für das angegebene Feld versucht wurde.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307826"
---
# <a name="update-function-access-custom-web-app"></a>Update-Funktion (Access Custom Web App)

Gibt zurück, ob ein Einfüge-oder Aktualisierungsvorgang für das angegebene Feld versucht wurde.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Update** (*Spalte*) 
  
Die **Update** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Column*  <br/> |Der Name des Felds, das auf einen Einfüge-oder Aktualisierungsvorgang überprüft werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **Update** -Funktion gibt true zurück, unabhängig davon, ob ein INSERT-oder Update-Versuch erfolgreich war. 
  

