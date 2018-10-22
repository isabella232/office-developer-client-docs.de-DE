---
title: CompareBookmarks-Methode (ADO)
TOCTitle: CompareBookmarks Method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fc4cf3540d22d3981bb13a7af3251dd625c2c99
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606248"
---
# <a name="comparebookmarks-method-ado"></a>CompareBookmarks-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013

Vergleicht zwei Textmarken und gibt einen Hinweis zu ihren relativen Werten zurück.

## <a name="syntax"></a>Syntax

*Ergebnis* = *Recordset-Objekt*. CompareBookmarks (*Bookmark1*, *Bookmark2*)

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt einen [CompareEnum](compareenum.md)-Wert zurück, der die relative Zeilenposition von zwei Datensätzen angibt, die durch ihre Textmarken dargestellt werden.

## <a name="parameters"></a>Parameter

  - *Bookmark1*

  - Die Textmarke der ersten Zeile.

  - *Bookmark2*

  - Die Textmarke der zweiten Zeile.

## <a name="remarks"></a>Hinweise

Die Textmarken müssen auf dasselbe [Recordset](recordset-object-ado.md)-Objekt oder auf ein **Recordset** -Objekt und dessen [Klon](clone-method-ado.md) angewendet werden. Sie können Textmarken aus verschiedenen **Recordset** -Objekten nicht zuverlässig vergleichen, selbst wenn sie von derselben Quelle oder demselben Befehl erstellt wurden. Sie können auch keine Textmarken für ein **Recordset** -Objekt vergleichen, wenn dessen zugrundeliegender Anbieter Vergleiche nicht unterstützt.

Eine Textmarke identifiziert eine Zeile in einem **Recordset** -Objekt eindeutig. Verwenden Sie die [Bookmark](bookmark-property-ado.md)-Eigenschaft der aktuellen Zeile, um deren Textmarke abzurufen.

Da der Datentyp einer Textmarke anbieterspezifisch ist, gibt ADO sie als einen Variant-Wert. SQL Server-Textmarken sind beispielsweise vom Typ DATENBANKTYP\_R8 (Double). ADO würde als einen Variant-Wert mit dem Untertyp Double dieses Typs verfügbar machen.

Beim Vergleichen von Textmarken werden von ADO keine Umwandlungen vorgenommen. Die Werte werden einfach an den Anbieter übergeben, bei dem der Vergleich durchgeführt wird. Wenn an die **CompareBookmarks** -Methode übergebene Textmarken in Variablen unterschiedlichen Typs gespeichert sind, wird möglicherweise der folgende Typkonfliktfehler generiert: "Die Argumente weisen einen falschen Typ auf, liegen außerhalb des gültigen Bereichs oder führen untereinander zu Konflikten".

Eine Textmarke, die ungültig oder falsch formatiert ist, verursacht einen Fehler.
