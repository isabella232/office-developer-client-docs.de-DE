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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709551"
---
# <a name="pagesize-property-ado"></a>PageSize-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt an, aus wie vielen Datensätze eine Seite im [Recordset](recordset-object-ado.md) besteht.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen Long-Wert fest, der angibt, wie viele Datensätze sich auf einer Seite befinden. Der Standardwert ist 10.

## <a name="remarks"></a>Hinweise

Mit der **PageSize** -Eigenschaft bestimmen Sie, aus wie vielen Datensätzen eine logische Datenseite besteht. Durch das Einrichten einer Seitengröße können Sie mit der [AbsolutePage](absolutepage-property-ado.md)-Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren. Dies ist nützlich in Szenarien, Web Server, wenn Sie den Benutzer zur Seite durch Daten sowie zulassen, jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen möchten.

Diese Eigenschaft kann jederzeit festgelegt werden. Mit ihrem Wert wird berechnet, wo sich der erste Datensatz auf einer bestimmten Seite befindet.

