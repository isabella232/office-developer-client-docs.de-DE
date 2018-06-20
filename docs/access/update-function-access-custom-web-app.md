---
title: Update-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Gibt zurück, ob ein Vorgang einfügen oder aktualisieren für das angegebene Feld versucht wurde.
ms.openlocfilehash: 1685d9f44bd167571b949a34d6c7b6993e63fbc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790390"
---
# <a name="update-function-access-custom-web-app"></a>Update-Funktion (Access benutzerdefinierte Web app)

Gibt zurück, ob ein Vorgang einfügen oder aktualisieren für das angegebene Feld versucht wurde.
  
> [!NOTE]
> [!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **Update** (*Spalte*) 
  
Die **Update** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Column*  <br/> |Der Name des Felds, das prüfen, ob einer Operation einfügen oder aktualisieren.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **Update** -Funktion gibt TRUE zurück, unabhängig davon, ob ein INSERT oder UPDATE erfolgreich hergestellt werden kann. 
  

