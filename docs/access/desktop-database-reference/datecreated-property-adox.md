---
title: DateCreated-Eigenschaft (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294421"
---
# <a name="datecreated-property-adox"></a>DateCreated-Eigenschaft (ADOX)


**Gilt für**: Access 2013, Office 2013

Gibt das Erstellungsdatum des Objekts an.

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaft gibt einen **Variant**-Wert zurück, der das Erstellungsdatum angibt. Der Wert ist Null, wenn **DateCreated** nicht vom Anbieter unterstützt wird.

## <a name="remarks"></a>Bemerkungen

Die **DateCreated**-Eigenschaft ist Null für neu angefügte Objekte. Nach Anfügen eines neuen [View](view-object-adox.md)- oder [Procedure](procedure-object-adox.md)-Objekts, müssen Sie die [Refresh](refresh-method-ado.md)-Methode der [Views](views-collection-adox.md)- oder [Procedures](procedures-collection-adox.md)-Auflistung aufrufen, um Werte für die **DateCreated**-Eigenschaft abzurufen.

