---
title: Relations.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: d71cecf2-da90-5f62-9e51-f994e660ad34
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835058(v=office.15)
ms:contentKeyID: 48547997
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fea6525d56552129ddc697cd56adf1eb6409345
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891037"
---
# <a name="relationsrefresh-method-dao"></a>Relations.Refresh Method (DAO)


**Betrifft**: Access 2013, Office 2013

Aktualisiert die Objekte in der angegebenen Auflistung, um das aktuelle Schema der Datenbank wiederzugeben.

## <a name="syntax"></a>Syntax

*Ausdruck* . Aktualisieren

*Ausdruck* Eine Variable, die ein **Relations** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **Refresh**-Methode in Mehrbenutzerumgebungen, in denen andere Benutzer auf die Datenbank zugreifen können. Außerdem bietet sich diese Methode für Auflistungen an, die indirekt von Änderungen an der Datenbank betroffen sind. Wenn Sie beispielsweise eine **Users**-Auflistung ändern, müssen Sie evtl. vor dem Verwenden der **Groups**-Auflistung eine **Groups**-Auflistung aktualisieren.

Eine Sammlung ist mit Objekten gefüllt, wenn das erste Mal darauf verwiesen wird. Nachfolgende Änderungen durch andere Benutzer werden nicht automatisch angezeigt. Wenn es wahrscheinlich ist, dass ein anderer Benutzer eine Auflistung geändert hat, wenden Sie sofort die Refresh-Methode auf die Auflistung an, bevor Sie eine Aufgabe in der Anwendung ausführen, die voraussetzt, dass ein bestimmtes Objekt in der Auflistung vorhanden ist bzw. fehlt. So ist sichergestellt, dass die Auflistung möglichst aktuell ist. Andererseits kann die Refresh-Methode die Leistung unnötigerweise beeinträchtigen.


