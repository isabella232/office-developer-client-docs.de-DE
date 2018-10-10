---
title: TableDef.DateCreated Property (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ffad5b1bee5756c969f03a920f453f1d3abf9e3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473311"
---
# <a name="tabledefdatecreated-property-dao"></a>TableDef.DateCreated Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Gibt das Datum und die Uhrzeit der Objekterstellung zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Variant**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . DateCreated

*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

DateCreated und LastUpdated geben das Datum und die Uhrzeit der Erstellung oder der letzen Aktualisierung des Objekts zurück. In einer Mehrbenutzerumgebung sollten Benutzer diese Einstellungen direkt vom Dateiserver erhalten, um Diskrepanzen bei den Einstellungen der Eigenschaften DateCreated und LastUpdated zu vermeiden.

