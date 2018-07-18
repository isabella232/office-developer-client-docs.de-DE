---
title: EOMonth-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Gibt den letzten Tag im Monat vor oder eine bestimmte Anzahl von Monaten zurück.
ms.openlocfilehash: cee42c4e5cb3a24b2e702673238ac9ee09bc7372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790182"
---
# <a name="eomonth-function-access-custom-web-app"></a>EOMonth-Funktion (Access benutzerdefinierte Web app)

Gibt den letzten Tag im Monat vor oder eine bestimmte Anzahl von Monaten zurück.
  
> [!NOTE]
> [!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **EOMonth** (*Datum*, *NumberOfMonth*) 
  
Die **EOMonth** enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Das Startdatum in Datums-/Uhrzeitformat oder in einer akzeptierten Textdarstellung eines Datums.  <br/> |
| *NumberOfMonth*  <br/> |Eine Zahl, die die Anzahl der Monate vor oder nach dem *Datum* darstellt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn *Datum* kein gültiges Datum vorliegt, gibt **EOMonth** einen Fehler zurück. 
  
Wenn *Datum* plus *NumberOfMonth* versatztage ein ungültiges Datum, gibt **EOMonth** einen Fehler zurück. 
  

