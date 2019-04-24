---
title: TableDefs. Refresh-Methode (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6050e2d0b97421bda7a2914f068db4019459ee7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306314"
---
# <a name="tabledefsrefresh-method-dao"></a>TableDefs. Refresh-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

Aktualisiert die Objekte in der angegebenen Auflistung, um das aktuelle Schema der Datenbank wiederzugeben.

## <a name="syntax"></a>Syntax

*Ausdruck* . Aktualisieren

*Ausdruck* Eine Variable, die ein **Tabledefs** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **OrdinalPosition**-Eigenschaft der einzelnen **Field**-Objekte, um die Position zu bestimmen, die das Microsoft Access-Datenbankmodul für **Field**-Objekte in der **Fields**-Auflistung eines **QueryDef**-, **Recordset**- oder **TableDef**-Objekts verwendet. Eine Änderung der **OrdinalPosition**-Eigenschaft eines **Field**-Objekts führt möglicherweise erst beim Anwenden der **Refresh**-Methode zu einer geänderten Reihenfolge der **Field**-Objekte.

Verwenden Sie die **Refresh**-Methode in Mehrbenutzerumgebungen, in denen andere Benutzer auf die Datenbank zugreifen können. Außerdem bietet sich diese Methode für Auflistungen an, die indirekt von Änderungen an der Datenbank betroffen sind. Wenn Sie beispielsweise eine **Users**-Auflistung ändern, müssen Sie evtl. vor dem Verwenden der **Groups**-Auflistung eine **Groups**-Auflistung aktualisieren.

A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.

