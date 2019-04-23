---
title: PageSize-Eigenschaft (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288133"
---
# <a name="pagesize-property-ado"></a>PageSize-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt an, aus wie vielen Datensätze eine Seite im [Recordset](recordset-object-ado.md) besteht.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.

## <a name="remarks"></a>Bemerkungen

Mit der **PageSize**-Eigenschaft bestimmen Sie, aus wie vielen Datensätzen eine logische Datenseite besteht. Durch das Einrichten einer Seitengröße können Sie mit der [AbsolutePage](absolutepage-property-ado.md)-Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren. Dies ist in Webserver Szenarios hilfreich, wenn Sie dem Benutzer erlauben möchten, über Daten zu blättern und gleichzeitig eine bestimmte Anzahl von Datensätzen anzuzeigen.

Diese Eigenschaft kann jederzeit festgelegt werden. Mit dem Wert dieser Eigenschaft wird die Position des ersten Datensatzes einer bestimmten Seite berechnet.

