---
title: Field.VisibleValue-Eigenschaft (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5b99b60edbe6b14091a81cf9f48c6a894932b083
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622333"
---
# <a name="fieldvisiblevalue-property-dao"></a>Field.VisibleValue-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . VisibleValue

*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält den Wert des Felds, der sich aktuell in der Datenbank auf dem Server befindet. Bei einer optimistischen Batchaktualisierung können Konflikte auftreten, wenn in der Zeitspanne, in der ein erster Client Daten abruft und eine Aktualisierung versucht, ein zweiter Client dasselbe Feld und den Datensatz ändert. In diesem Fall kann über diese Eigenschaft auf den vom zweiten Client festgelegten Wert zugegriffen werden.

