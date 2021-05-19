---
title: Update-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Gibt zurück, ob ein INSERT- oder UPDATE-Vorgang für das angegebene Feld versucht wurde.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410917"
---
# <a name="update-function-access-custom-web-app"></a>Update-Funktion (benutzerdefinierte Access-Web-App)

Gibt zurück, ob ein INSERT- oder UPDATE-Vorgang für das angegebene Feld versucht wurde.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Update** (*Column*) 
  
Die **Update-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Column*  <br/> |Der Name des Felds, das auf einen INSERT- oder UPDATE-Vorgang überprüft werden soll.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **Update-Funktion** gibt TRUE zurück, unabhängig davon, ob ein INSERT- oder UPDATE-Versuch erfolgreich war. 
  

