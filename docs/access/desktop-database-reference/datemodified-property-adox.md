---
title: DateModified-Eigenschaft (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daf72804d51c18b5875e607ce5fdb0dfe20f406c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294407"
---
# <a name="datemodified-property-adox"></a>DateModified-Eigenschaft (ADOX)


**Gilt für**: Access 2013, Office 2013

Gibt das Datum an, an dem das Objekt zuletzt geändert wurde.

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaft gibt einen **Variant** -Wert zurück, der das Änderungsdatum angibt. Der Wert ist Null, wenn **DateModified** nicht vom Anbieter unterstützt wird.

## <a name="remarks"></a>Bemerkungen

Die **DateModified**-Eigenschaft ist Null für neu angefügte Objekte. Nach Anfügen eines neuen [View](view-object-adox.md)- oder [Procedure](procedure-object-adox.md)-Objekts, müssen Sie die [Refresh](refresh-method-ado.md)-Methode der [Views](views-collection-adox.md)- oder [Procedures](procedures-collection-adox.md)-Auflistung aufrufen, um Werte für die **DateModified**-Eigenschaft abzurufen.

