---
title: CompareBookmarks-Methode (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3439cb1a15d98c8e0b882ef8ba0bfd3e934f689a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612281"
---
# <a name="comparebookmarks-method-ado"></a>CompareBookmarks-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Vergleicht zwei Textmarken und gibt einen Hinweis zu ihren relativen Werten zurück.

## <a name="syntax"></a>Syntax

*Ergebnis*  =  *Recordset*. CompareBookmarks(*Bookmark1*, *Bookmark2*)

## <a name="return-value"></a>Rückgabewert

Gibt einen [CompareEnum](compareenum.md)-Wert zurück, der die relative Zeilenposition von zwei Datensätzen angibt, die durch ihre Textmarken dargestellt werden.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Bookmark1* |Die Textmarke der ersten Zeile.|
|*Bookmark2* |Die Textmarke der zweiten Zeile.|

## <a name="remarks"></a>HinwBemerkungeneise

Die Textmarken müssen auf dasselbe [Recordset](recordset-object-ado.md)-Objekt oder auf ein **Recordset** -Objekt und dessen [Klon](clone-method-ado.md) angewendet werden. Sie können Textmarken aus verschiedenen **Recordset** -Objekten nicht zuverlässig vergleichen, selbst wenn sie von derselben Quelle oder demselben Befehl erstellt wurden. Sie können auch keine Textmarken für ein **Recordset** -Objekt vergleichen, wenn dessen zugrundeliegender Anbieter Vergleiche nicht unterstützt.

Eine Textmarke identifiziert eine Zeile in einem **Recordset** -Objekt eindeutig. Verwenden Sie die [Bookmark](bookmark-property-ado.md)-Eigenschaft der aktuellen Zeile, um deren Textmarke abzurufen.

Because the data type of a bookmark is provider specific, ADO exposes it as a Variant. SQL Server Lesezeichen sind beispielsweise vom Typ DBTYPE \_ R8 (Double). ADO would expose this type as a Variant with a subtype of Double.

Beim Vergleichen von Textmarken werden von ADO keine Umwandlungen vorgenommen. Die Werte werden einfach an den Anbieter übergeben, bei dem der Vergleich durchgeführt wird. Wenn an die **CompareBookmarks** -Methode übergebene Textmarken in Variablen unterschiedlichen Typs gespeichert sind, wird möglicherweise der folgende Typkonfliktfehler generiert: "Die Argumente weisen einen falschen Typ auf, liegen außerhalb des gültigen Bereichs oder führen untereinander zu Konflikten".

Eine Textmarke, die ungültig oder falsch formatiert ist, verursacht einen Fehler.

