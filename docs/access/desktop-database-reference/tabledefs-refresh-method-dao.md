---
title: TableDefs.Refresh-Methode (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 53a632999f1b60b078e9365c9f99e52ddec284e9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927879"
---
# <a name="tabledefsrefresh-method-dao"></a>TableDefs.Refresh-Methode (DAO)


**Betrifft**: Access 2013, Office 2013

Aktualisiert die Objekte in der angegebenen Auflistung, um das aktuelle Schema der Datenbank wiederzugeben.

## <a name="syntax"></a>Syntax

*Ausdruck* . Aktualisieren

*Ausdruck* Eine Variable, die ein **TableDefs** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **OrdinalPosition**-Eigenschaft der einzelnen **Field**-Objekte, um die Position zu bestimmen, die das Microsoft Access-Datenbankmodul für **Field**-Objekte in der **Fields**-Auflistung eines **QueryDef**-, **Recordset**- oder **TableDef**-Objekts verwendet. Eine Änderung der **OrdinalPosition**-Eigenschaft eines **Field**-Objekts führt möglicherweise erst beim Anwenden der **Refresh**-Methode zu einer geänderten Reihenfolge der **Field**-Objekte.

Verwenden Sie die **Refresh**-Methode in Mehrbenutzerumgebungen, in denen andere Benutzer auf die Datenbank zugreifen können. Außerdem bietet sich diese Methode für Auflistungen an, die indirekt von Änderungen an der Datenbank betroffen sind. Wenn Sie beispielsweise eine **Users**-Auflistung ändern, müssen Sie evtl. vor dem Verwenden der **Groups**-Auflistung eine **Groups**-Auflistung aktualisieren.

Eine Sammlung ist mit Objekten gefüllt, wenn das erste Mal darauf verwiesen wird. Nachfolgende Änderungen durch andere Benutzer werden nicht automatisch angezeigt. Wenn es wahrscheinlich ist, dass ein anderer Benutzer eine Auflistung geändert hat, wenden Sie sofort die Refresh-Methode auf die Auflistung an, bevor Sie eine Aufgabe in der Anwendung ausführen, die voraussetzt, dass ein bestimmtes Objekt in der Auflistung vorhanden ist bzw. fehlt. So ist sichergestellt, dass die Auflistung möglichst aktuell ist. Andererseits kann die Refresh-Methode die Leistung unnötigerweise beeinträchtigen.


