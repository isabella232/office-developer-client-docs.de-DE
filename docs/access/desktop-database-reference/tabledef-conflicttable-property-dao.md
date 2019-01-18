---
title: TableDef.ConflictTable-Eigenschaft (DAO)
TOCTitle: ConflictTable Property
ms:assetid: 0db8b975-eb6d-19c6-cfb7-6ce01230ebe4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845218(v=office.15)
ms:contentKeyID: 48543228
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053356
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0189a5163dd5e225ad34841264cf84e85785d7fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718917"
---
# <a name="tabledefconflicttable-property-dao"></a>TableDef.ConflictTable-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

Gibt den Name einer Konflikttabelle zurück, die die Datensätze der Datenbank enthält, die bei der Synchronisierung zweier Replikate einen Konflikt ausgelöst haben (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter **String**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . ConflictTable

*Ausdruck* Ein Ausdruck, der ein **TableDef** -Objekt zurückgibt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert ist vom Datentyp **String** mit einer leeren Zeichenfolge (""), wenn es keine Konflikttabelle gibt oder die Datenbank kein Replikat ist.

Wenn zwei Benutzer an zwei gesonderten Replikaten Änderungen an demselben Datensatz in der Datenbank vornehmen, können die Änderungen eines Benutzers nicht auf das andere Replikat angewendet werden. Folglich muss der Benutzer, dessen Änderungen fehlschlugen, die Konflikte auflösen.

Konflikte treten auf Datensatzebene auf, nicht zwischen Feldern. Wenn z. B. ein Benutzer das Adressfeld ändert und ein anderer Benutzer das Telefonnummernfeld desselben Datensatzes aktualisiert, wird eine Änderung abgelehnt. Da Konflikte auf der Datensatzebene auftreten, erfolgt die Ablehnung, obwohl die erfolgreiche Änderung und die abgelehnte Änderung kaum zu einem echten Informationskonflikt führen.

Der Synchronisierungsmechanismus verarbeitet die Datensatzkonflikte. Dabei werden Konflikttabellen erstellt, die die Informationen enthalten, die bei einer erfolgreichen Änderung in der Tabelle gespeichert worden wären. Sie können diese Konflikttabellen überprüfen und Zeile für Zeile die erforderlichen Korrekturen vornehmen.

Konflikttabellen heißen Tabelle\_Konflikt, wobei Tabelle der ursprüngliche Name der Tabelle ist, auf die maximal zulässige Länge gekürzt.

