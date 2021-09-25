---
title: PageSize-Eigenschaft (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 41a70c07939b979c632636352c5b0a642973b5e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562559"
---
# <a name="pagesize-property-ado"></a>PageSize-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt an, aus wie vielen Datensätze eine Seite im [Recordset](recordset-object-ado.md) besteht.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.

## <a name="remarks"></a>HinwBemerkungeneise

Mit der **PageSize**-Eigenschaft bestimmen Sie, aus wie vielen Datensätzen eine logische Datenseite besteht. Durch das Einrichten einer Seitengröße können Sie mit der [AbsolutePage](absolutepage-property-ado.md)-Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren. Dies ist in Webserverszenarien nützlich, wenn Sie dem Benutzer erlauben möchten, Daten zu durchsuchen und gleichzeitig eine bestimmte Anzahl von Datensätzen anzuzeigen.

Diese Eigenschaft kann jederzeit festgelegt werden. Mit dem Wert dieser Eigenschaft wird die Position des ersten Datensatzes einer bestimmten Seite berechnet.

