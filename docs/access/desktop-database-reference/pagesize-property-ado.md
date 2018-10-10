---
title: PageSize-Eigenschaft (ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473045"
---
# <a name="pagesize-property-ado"></a>PageSize-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, aus wie vielen Datensätze eine Seite im [Recordset](recordset-object-ado.md) besteht.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen Long-Wert fest, der angibt, wie viele Datensätze sich auf einer Seite befinden. Der Standardwert ist 10.

## <a name="remarks"></a>Hinweise

Mit der **PageSize** -Eigenschaft bestimmen Sie, aus wie vielen Datensätzen eine logische Datenseite besteht. Durch das Einrichten einer Seitengröße können Sie mit der [AbsolutePage](absolutepage-property-ado.md)-Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren. Dies ist für Webserverszenarien hilfreich, wenn Sie dem Benutzer gestatten möchten, in den Daten zu blättern und jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen.

Diese Eigenschaft kann jederzeit festgelegt werden. Mit ihrem Wert wird berechnet, wo sich der erste Datensatz auf einer bestimmten Seite befindet.

