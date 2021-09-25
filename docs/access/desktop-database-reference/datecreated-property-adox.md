---
title: DateCreated-Eigenschaft (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4a7df2a0b4d348402560c6781af80f56f55ecb9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585865"
---
# <a name="datecreated-property-adox"></a>DateCreated-Eigenschaft (ADOX)


**Gilt für**: Access 2013, Office 2013

Gibt das Erstellungsdatum des Objekts an.

## <a name="return-values"></a>Rückgabewerte

Diese Eigenschaft gibt einen **Variant**-Wert zurück, der das Erstellungsdatum angibt. Der Wert ist Null, wenn **DateCreated** nicht vom Anbieter unterstützt wird.

## <a name="remarks"></a>HinwBemerkungeneise

Die **DateCreated**-Eigenschaft ist Null für neu angefügte Objekte. Nach Anfügen eines neuen [View](view-object-adox.md)- oder [Procedure](procedure-object-adox.md)-Objekts, müssen Sie die [Refresh](refresh-method-ado.md)-Methode der [Views](views-collection-adox.md)- oder [Procedures](procedures-collection-adox.md)-Auflistung aufrufen, um Werte für die **DateCreated**-Eigenschaft abzurufen.

