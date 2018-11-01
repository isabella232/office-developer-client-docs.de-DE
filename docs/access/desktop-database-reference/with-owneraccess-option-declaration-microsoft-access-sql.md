---
title: WITH OWNERACCESS OPTION-Deklaration (Microsoft Access SQL)
TOCTitle: WITH OWNERACCESS OPTION Declaration (Microsoft Access SQL)
ms:assetid: 82e51071-12b2-e97e-07b4-27ffceda831e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196724(v=office.15)
ms:contentKeyID: 48545993
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277584
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0ef07e29258035486a89e1b2cc19519d3f2f7c9f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889966"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>WITH OWNERACCESS OPTION-Deklaration (Microsoft Access SQL)


**Betrifft**: Access 2013, Office 2013

In einer Mehrbenutzerumgebung mit einer sicheren Arbeitsgruppe wird diese Deklaration mit einer Abfrage verwendet, um dem Benutzer, der die Abfrage ausführt, dieselben Berechtigungen zuzuweisen wie dem Besitzer der Abfrage.

## <a name="syntax"></a>Syntax

*SQL-Anweisung* MIT OWNERACCESS OPTION

## <a name="remarks"></a>Hinweise

Die WITH OWNERACCESS OPTION-Deklaration ist optional.

Im folgenden Beispiel kann der Benutzer Gehaltsdaten anzeigen (selbst wenn der Benutzer normalerweise nicht über die Berechtigungen zum Anzeigen der Tabelle mit den Gehältern verfügt). Dies ist jedoch nur möglich, wenn der Besitzer der Abfrage über die entsprechende Berechtigung verfügt:

``` sql
SELECT LastName, 
FirstName, Salary
FROM Employees 
ORDER BY LastName 
WITH OWNERACCESS OPTION;
```

Wenn ein Benutzer aus anderen Gründen keine Tabelle erstellen kann oder einer Tabelle keine Daten hinzufügen kann, können Sie WITH OWNERACCESS OPTION verwenden, damit der Benutzer eine Tabellenerstellungs- oder Anfügeabfrage ausführen kann.

Wenn Sie die Sicherheitseinstellungen und Benutzerberechtigungen der Arbeitsgruppe durchsetzen möchten, sollten Sie die WITH OWNERACCESS OPTION-Deklaration nicht verwenden.

Diese Option erfordert, dass Sie auf die mit der Datenbank verknüpfte Datei System.mdw zugreifen können. Dies ist nur in einer sicheren Mehrbenutzerimplementation sinnvoll.

