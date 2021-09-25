---
title: NativeError-Eigenschaft (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5ff124266829cc4fe9f13d95c50cb2255eaa4591
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577248"
---
# <a name="nativeerror-property-ado"></a>NativeError-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den anbieterspezifischen Fehlercode für ein bestimmtes [Error](error-object-ado.md)-Objekt an.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long**-Wert zurück, der den Fehlercode angibt.

## <a name="remarks"></a>HinwBemerkungeneise

Rufen Sie mit der **NativeError**-Eigenschaft die datenbankspezifische Fehlerinformation für ein bestimmtes **Error**-Objekt ab. Wenn z. B. der Microsoft OLE DB-Anbieter für ODBC mit einer Microsoft SQL Server-Datenbank verwendet wird, werden systemeigene Fehlercodes, die aus SQL Server stammen, über ODBC und den ODBC-Anbieter an die **NativeError**-Eigenschaft übergeben.

