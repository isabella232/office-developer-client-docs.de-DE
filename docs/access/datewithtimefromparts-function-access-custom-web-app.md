---
title: DateWithTimeFromParts-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Gibt ein Datum und eine Uhrzeit basierend auf einem angegebenen Jahr, Monat, Tag und Uhrzeit zurück.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422089"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>DateWithTimeFromParts-Funktion (benutzerdefinierte Access-Web-App)

Gibt ein Datum und eine Uhrzeit basierend auf einem angegebenen Jahr, Monat, Tag und Uhrzeit zurück.
  
> [!NOTE]
> Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*) 
  
Die **DateWithTimeFromParts-Funktion** enthält die folgenden Argumente. 
  
|**Argumentname**|**Beschreibung**|
|:-----|:-----|
| *Jahr*  <br/> |Ganzzahliger Ausdruck, der ein Jahr an gibt.  <br/> |
| *Month*  <br/> |Ganzzahliger Ausdruck, der einen Monat an gibt.  <br/> |
| *Day*  <br/> |Ganzzahliger Ausdruck, der einen Tag an gibt.  <br/> |
| *Hour*  <br/> |Ganzzahliger Ausdruck, der Stunden an gibt.  <br/> |
| *Minute*  <br/> |Ganzzahliger Ausdruck, der Minuten an gibt.  <br/> |
| *Zweiter*  <br/> |Ganzzahliger Ausdruck, der Sekunden an gibt.  <br/> |
   
## <a name="remarks"></a>Hinweise

**DateWithTimeFromParts gibt** einen vollständig initialisierten Date/Time-Wert zurück. Wenn die Argumente ungültig sind, wird ein Fehler ausgelöst. Wenn erforderliche Argumente Null sind, wird Null zurückgegeben. 
  

