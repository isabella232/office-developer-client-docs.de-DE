---
title: DateWithTimeFromParts-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Gibt ein Datum und eine Uhrzeit basierend auf einem angegebenen Jahr, Monat, Tag und Uhrzeit zurück.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282141"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>DateWithTimeFromParts-Funktion (Access Custom Web App)

Gibt ein Datum und eine Uhrzeit basierend auf einem angegebenen Jahr, Monat, Tag und Uhrzeit zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateWithTimeFromParts** (*Jahr*, *Monat*, *Tag*, *Stunde*, *Minute*, *Sekunde*) 
  
Die **DateWithTimeFromParts** -Funktion enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Jahr*  <br/> |Integer-Ausdruck, der ein Jahr angibt.  <br/> |
| *Month*  <br/> |Integer-Ausdruck, der einen Monat angibt.  <br/> |
| *Day*  <br/> |Integer-Ausdruck, der einen Tag angibt.  <br/> |
| *Hour*  <br/> |Integer-Ausdruck, der Stunden angibt.  <br/> |
| *Minute*  <br/> |Ganzzahliger Ausdruck, der Minuten angibt.  <br/> |
| *Zweiter*  <br/> |Integer-Ausdruck, der Sekunden angibt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

**DateWithTimeFromParts** gibt einen vollständig initialisierten Datum/Uhrzeit-Wert zurück. Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst. Wenn die erforderlichen Argumente NULL sind, wird NULL zurückgegeben. 
  

