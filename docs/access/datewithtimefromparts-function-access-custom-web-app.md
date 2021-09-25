---
title: DateWithTimeFromParts-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Gibt Datum und Uhrzeit basierend auf einem angegebenen Jahr, Monat, Tag und Uhrzeit zurück.
ms.openlocfilehash: ed1554ed6fa03dd75f290f502fbf0c0a02b02b15
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586446"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>DateWithTimeFromParts-Funktion (benutzerdefinierte Access-Web-App)

Gibt Datum und Uhrzeit basierend auf einem angegebenen Jahr, Monat, Tag und Uhrzeit zurück.
  
> [!NOTE]
> Das in diesem Artikel beschriebene Cloudspeicherfeature wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann zu folgendem Fehler führen: > *Leider haben wir Serverprobleme, daher können wir es jetzt nicht \<service\> hinzufügen. Versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*) 
  
Die **DateWithTimeFromParts-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Jahr*  <br/> |Ganzzahliger Ausdruck, der ein Jahr angibt.  <br/> |
| *Month*  <br/> |Ganzzahliger Ausdruck, der einen Monat angibt.  <br/> |
| *Day*  <br/> |Ganzzahliger Ausdruck, der einen Tag angibt.  <br/> |
| *Hour*  <br/> |Ganzzahliger Ausdruck, der Stunden angibt.  <br/> |
| *Minute*  <br/> |Ganzzahliger Ausdruck, der Minuten angibt.  <br/> |
| *Zweiter*  <br/> |Ganzzahliger Ausdruck, der Sekunden angibt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

**DateWithTimeFromParts** gibt einen vollständig initialisierten Date/Time-Wert zurück. Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst. Wenn erforderliche Argumente Null sind, wird Null zurückgegeben. 
  

