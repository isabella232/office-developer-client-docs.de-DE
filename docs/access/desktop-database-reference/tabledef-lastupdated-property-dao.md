---
title: TableDef.LastUpdated-Eigenschaft (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0f6d3dd46de36ef374372d9463a89b223e9ed946
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562167"
---
# <a name="tabledeflastupdated-property-dao"></a>TableDef.LastUpdated-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt das Datum und die Uhrzeit der letzten Änderung eines Objekts zurück. Schreibgeschützter **Variant**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . LastUpdated

*Ausdruck* Eine Variable, die ein **TableDef**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.

