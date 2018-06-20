---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Verwenden Sie zum Öffnen der Schlingern Anwendung und anzeigen oder bearbeiten eine Schlingern das Sway URI-Schema.
ms.openlocfilehash: 7a820339abcd666e7e1b9ad584cd152ca8fd4f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796376"
---
# <a name="sway-uri-scheme"></a>Sway URI-Schema

Dieses Dokument definiert das Format des Uniform Resource Identifiers (URIs) für die Anwendung Schlingern für Windows. Dieser URI-Schema können Sie die Anwendung Schlingern mit verschiedenen Befehlen aufrufen.

## <a name="sway-uri-scheme-syntax"></a>Die Syntax der URI-Schema sway

Dies ist die URI-Schema-Syntax:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash; Gibt an, dass Schlingern Anwendung, die aufgerufen wird. Bei der Installation von Sway für Windows `ms-sway` mit der Schlingern Handler für Windows registriert ist.
- `<command-argument>`&ndash; A URI möglicherweise ein oder mehrere Befehlsargumente, getrennt durch das kaufmännische und-Zeichen (`&`) Zeichen. Wenn mehr als ein Befehlsargument in einem URI, ein kaufmännisches und-Zeichen enthalten ist (`&`) Zeichen muss jede Befehlsargument aus dem folgenden Befehlsargument verwendet. Befehlsargumente variieren je nach Szenario. 

## <a name="command-arguments"></a>Befehlsargumente

Mehrere Befehlsargumente können in das Sway URL-Schema enthalten sein. Dieser Befehlsargumenten sind nicht erforderlich. Wenn Sie nicht die Befehlsargumenten verwenden, wird die Anwendung Schlingern aufgerufen.

|Befehlsnamen argument|Beschreibung|Typ|Mögliche Werte|Erforderlich?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|Der eindeutige Bezeichner der einer Schlingern. Verwendet, um anzugeben, die Schlingern geöffnet werden soll.|String|Ein gültiger Eindeutiger Bezeichner für eine Schlingern. Die Id ist immer Teil der URL zu einer Schlingern.<br/><br/>Zum Beispiel für die folgenden Schlingern `https://sway.com/dBheQgVZ1RQBfiQU`, die Id lautet `dBheQgVZ1RQBfiQU`.<br/><br/>Wenn das Benutzerkonto, das die Schlingern-Anwendung gehörigen Bearbeitungsberechtigungen verfügt, wird die Anwendung die Schlingern im Bearbeitungsmodus geöffnet. Andernfalls wird die Anwendung die Schlingern im Ansichtsmodus geöffnet.|Nein|
|**mode**|Der Modus, in dem eine bestimmte Schlingern geöffnet, zur Bearbeitung oder zur Anzeige werden soll.|String|Bearbeiten<br/>Ansicht<br/><br/>**Hinweis**: dieser Befehlsargument wird ignoriert, wenn keine **Id** angegeben wird,.|Nein|
|**auth_upn**|Das Konto beim Öffnen von Schlingern verwendet.|String|Eine gültige e-Mail-Adresse.<br/><br/>Wenn die angegebene e-Mail-Adresse nicht mit einem Konto Schlingern verknüpft ist, wird der Benutzer als der angegebene Benutzer anmelden von Schlingern gefragt.<br/><br/>Wenn mehr als ein Konto Schlingern-Anwendung zugeordnet ist, und die angegebene e-Mail-Adresse vorhanden ist, wechselt die Schlingern-Anwendung, die mit diesem Konto beim Aufrufen.|Nein|
|**Auth\_Pvr**|Die Art des Kontos zum Öffnen der Schlingern&mdash;ein Microsoft-Konto oder einem Azure Active Directory-Konto (Azure AD).|String|WindowsLiveId – gibt an, dass die **Auth\_Upn** Konto ist ein Microsoft-Konto.<br/><br/>Organisations-ID – gibt an, dass die **Auth\_Upn** Konto ist ein Azure AD-Konto.<br/><br/>Wenn kein **Auth\_Upn** angegeben wird, ist dieses Befehlsargument wird ignoriert.|Nein|
|**Aufrufen von\_app**|Der Name der Windows-Anwendung verwendet, um Schlingern aufzurufen.|String|Der Anzeigename der Windows-Anwendung verwendet, um über das Sway URL-Schema Schlingern aufzurufen.<br/><br/>Der Zweck dieses Befehlsargument ist für Telemetrie und Nachverfolgen von Änderungen.|Nein|

## <a name="uri-scheme-semantics"></a>Semantik der URI-Schema

Die `<ms-sway>` Schema definiert eine URI-Syntax zum Öffnen einer Schlingern oder für die Anwendung Schlingern aufrufen. Das Schema definiert mehrere Befehlsargumente, die verwendet werden kann, um Folgendes auszuführen: 

- Öffnen Sie die Anwendung Schlingern &ndash; keine Befehlsargumente müssen angegeben werden. 

- Öffnen Sie ein Schlingern für die Anzeige in der Anwendung Schlingern &ndash; die **-Id** und - **Modus** anzeigen müssen angegeben werden. 

- Öffnen Sie ein Schlingern zur Bearbeitung in der Anwendung Schlingern &ndash; legen Sie die **Id** und den **Modus** bearbeiten muss angegeben werden. Es wird empfohlen, dass Sie auch einschließen **Auth\_Upn** und **Auth\_Pvr** zur Sicherstellung, dass das richtige Konto mit Berechtigungen bearbeiten verwendet wird, wenn Schlingern geöffnet wird.  

## <a name="example"></a>Beispiel

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


