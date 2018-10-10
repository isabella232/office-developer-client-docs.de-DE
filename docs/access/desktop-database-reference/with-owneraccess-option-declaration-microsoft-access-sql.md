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
ms.openlocfilehash: b47b9fcc5b3c4422ec60bbdaf06193533c20b6e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475522"
---
# <a name="with-owneraccess-option-declaration-microsoft-access-sql"></a>WITH OWNERACCESS OPTION-Deklaration (Microsoft Access SQL)


**Betrifft**: Access 2013 | Office 2013

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

