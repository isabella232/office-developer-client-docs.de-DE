---
title: DateWithTimeFromParts-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Gibt ein Datum und einen Zeitraum basierend auf einer angegebenen Jahr, Monat, Tag und Uhrzeit.
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790161"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>DateWithTimeFromParts-Funktion (Access benutzerdefinierte Web app)

Gibt ein Datum und einen Zeitraum basierend auf einer angegebenen Jahr, Monat, Tag und Uhrzeit.
  
> [!NOTE]
> [!HINWEIS] Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateWithTimeFromParts** (*Jahr*, *Monat*, *Tag*, *Stunde*, *Minute*, *Sekunde*) 
  
Die **DateWithTimeFromParts** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Description**|
|:-----|:-----|
| *Jahr*  <br/> |Ein Ausdruck, der ganze Zahl, die einem Jahr angibt.  <br/> |
| *Month*  <br/> |Ein Ausdruck, der ganze Zahl, die einen Monat angibt.  <br/> |
| *Tag*  <br/> |Ein Ausdruck, der ganze Zahl, die einen Tag angibt.  <br/> |
| *Stunde*  <br/> |Integer-Ausdruck Stunden angeben.  <br/> |
| *Minute*  <br/> |Integer-Ausdruck Minuten angeben.  <br/> |
| *Sekunde*  <br/> |Integer-Ausdruck Sekunden angeben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

**DateWithTimeFromParts** gibt einen vollständig initialisierten Datums-/Zeitwert zurück. Wenn die Argumente nicht gültig sind, wird ein Fehler ausgelöst. Falls erforderlich, dass Argumente Null sind, wird Null zurückgegeben. 
  

