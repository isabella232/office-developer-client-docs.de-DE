---
title: Field2.VisibleValue-Eigenschaft (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 82e3e113290bd34adfcf79e5bc429c539c757f29
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626694"
---
# <a name="field2visiblevalue-property-dao"></a>Field2.VisibleValue-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . VisibleValue

*Ausdruck* Eine Variable, die ein **Field2**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält den Wert des Felds, der sich aktuell in der Datenbank auf dem Server befindet. Bei einer optimistischen Batchaktualisierung können Konflikte auftreten, wenn in der Zeitspanne, in der ein erster Client Daten abruft und eine Aktualisierung versucht, ein zweiter Client dasselbe Feld und den Datensatz ändert. In diesem Fall kann über diese Eigenschaft auf den vom zweiten Client festgelegten Wert zugegriffen werden.

