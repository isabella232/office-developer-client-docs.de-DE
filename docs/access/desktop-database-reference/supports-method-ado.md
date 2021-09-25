---
title: Supports-Methode (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9551120657b2284959f1f7c69d8a11324ea9e5e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585256"
---
# <a name="supports-method-ado"></a>Supports-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Bestimmt, ob ein angegebenes [Recordset](recordset-object-ado.md)-Objekt einen bestimmten Funktionalitätstyp unterstützt.

## <a name="syntax"></a>Syntax

*Boolescher Wert*  =  *Recordset*. Supports (*CursorOptions*)

## <a name="return-value"></a>Rückgabewert

Gibt einen **Boolean**-Wert zurück, der kennzeichnet, ob alle vom *CursorOptions*-Argument identifizierten Features vom Anbieter unterstützt werden.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*CursorOptions* |Ein Ausdruck vom Datentyp **Long**, der aus mindestens einem [CursorOptionEnum](cursoroptionenum.md)-Wert besteht.|

## <a name="remarks"></a>HinwBemerkungeneise

Mit der **Supports**-Methode bestimmen Sie, welche Funktionalität ein **Recordset**-Objekt unterstützt. Wenn das **Recordset**-Objekt die Features unterstützt, deren entsprechende Konstanten in *CursorOptions* enthalten sind, gibt die **Supports**-Methode **True** zurück. Andernfalls wird **False** zurückgegeben.


> [!NOTE]
> [!HINWEIS] Die **Supports** -Methode kann zwar **True** für eine bestimmte Funktionalität zurückgeben, aber dies garantiert nicht, dass der Anbieter das Feature unter allen Umständen zur Verfügung stellen kann. Die **Supports** -Methode gibt einfach zurück, ob der Anbieter die angegebene Funktionalität unterstützen kann, vorausgesetzt bestimmte Bedingungen sind erfüllt. Beispielsweise kann die **Supports** -Methode angeben, dass ein **Recordset** -Objekt Aktualisierungen unterstützt, obwohl der Cursor auf einer Verknüpfung mehrerer Tabellen basiert, von denen manche Spalten nicht aktualisierbar sind.


