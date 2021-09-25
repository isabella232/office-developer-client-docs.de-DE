---
title: QueryDef.DateCreated-Eigenschaft (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 626b5f980369f5b4bf4b24579af0aa7ed308343f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617798"
---
# <a name="querydefdatecreated-property-dao"></a>QueryDef.DateCreated-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt das Datum und die Uhrzeit der Objekterstellung zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Variant**-Wert.

## <a name="syntax"></a>Syntax

*Ausdruck* . Datecreated

*Ausdruck* Eine Variable, die ein **QueryDef**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.

