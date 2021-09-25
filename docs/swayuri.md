---
title: SwayURI
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 11daa75b-87fc-4e63-8e02-09ab9307c8f8
ms.date: 01/28/2016
description: Verwenden Sie das Sway-URI-Schema, um die Sway-Anwendung zu öffnen und ein Sway anzuzeigen oder zu bearbeiten.
ms.openlocfilehash: 10357bd7df8bd0bff96e042cb715c0a691a31a9c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560186"
---
# <a name="sway-uri-scheme"></a>Sway-URI-Schema

In diesem Dokument wird das Format der URIs (Uniform Resource Identifiers) für die Sway-Anwendung für Windows definiert. Sie können dieses URI-Schema verwenden, um die Sway-Anwendung mit verschiedenen Befehlen aufzurufen.

## <a name="sway-uri-scheme-syntax"></a>Sway-URI-Schemasyntax

Es folgt die URI-Schemasyntax:

`<ms-sway>:<command-argument>`

- `<ms-sway>`&ndash;Gibt an, dass Sway die aufzurufende Anwendung ist. Wenn Sway für Windows installiert ist, `ms-sway` wird bei Windows als Sway-Handler registriert.
- `<command-argument>`&ndash;Ein URI kann ein oder mehrere Befehlsargumente aufweisen, die durch das kaufmännische Und-Zeichen () getrennt `&` sind. Wenn mehrere Befehlsargumente in einem URI enthalten sind, muss jedes Befehlsargument durch ein kaufmännisches `&` Und-Zeichen () vom folgenden Befehlsargument getrennt werden. Befehlsargumente variieren je nach Szenario. 

## <a name="command-arguments"></a>Befehlsargumente

Mehrere Befehlsargumente können als Teil des Sway-URL-Schemas eingeschlossen werden. Diese Befehlsargumente sind nicht erforderlich. Wenn Sie die Befehlsargumente nicht angeben, wird die Sway-Anwendung aufgerufen.

|Name des Befehlsarguments|Beschreibung|Typ|Mögliche Werte|Pflichtfeld?|
|:-----|:-----|:-----|:-----|:-----|
|**id**|Der eindeutige Bezeichner eines Sways. Wird verwendet, um das zu öffnende Sway anzugeben.|String|Ein gültiger eindeutiger Bezeichner für ein Sway. Die ID ist immer Teil der URL zu einem Sway.<br/><br/>For example, for the following Sway `https://sway.com/dBheQgVZ1RQBfiQU` , the ID is `dBheQgVZ1RQBfiQU` .<br/><br/>Wenn das der Sway-Anwendung zugeordnete Benutzerkonto über Bearbeitungsberechtigungen verfügt, öffnet die Anwendung das Sway im Bearbeitungsmodus. Andernfalls öffnet die Anwendung das Sway im Ansichtsmodus.|Nein|
|**mode**|Der Modus, in dem ein bestimmtes Sway geöffnet werden soll, ob zum Bearbeiten oder zum Anzeigen.|String|Bearbeiten<br/>Ansicht<br/><br/>**HINWEIS:** Wenn keine **ID** angegeben ist, wird dieses Befehlsargument ignoriert.|Nein|
|**auth_upn**|Das Konto, das beim Öffnen von Sway verwendet werden soll.|String|Eine gültige E-Mail-Adresse.<br/><br/>Wenn die angegebene E-Mail-Adresse keinem Sway-Konto zugeordnet ist, fordert Sway den Benutzer auf, sich als angegebener Benutzer anzumelden.<br/><br/>Wenn der Sway-Anwendung mehr als ein Konto zugeordnet ist und die angegebene E-Mail-Adresse vorhanden ist, wechselt die Sway-Anwendung beim Aufrufen zu diesem Konto.|Nein|
|**auth \_ pvr**|Der Kontotyp, der zum Öffnen des Sways verwendet werden soll, &mdash; entweder ein Microsoft-Konto oder ein Azure Active Directory Konto (Azure AD).|String|WindowsLiveId – Gibt an, dass das **Authentifizierungskonto \_** ein Microsoft-Konto ist.<br/><br/>OrgId – Gibt an, dass das **Authentifizierungskonto \_** ein Azure AD-Konto ist.<br/><br/>Wenn kein **\_ Authentifizierungs-Upn** angegeben ist, wird dieses Befehlsargument ignoriert.|Nein|
|**Aufrufen der \_ App**|Der Name der Windows Anwendung, die zum Aufrufen von Sway verwendet wird.|String|Der Anzeigename der Windows Anwendung, die zum Aufrufen von Sway über das Sway-URL-Schema verwendet wird.<br/><br/>Der Zweck dieses Befehlsarguments ist für Telemetrie und Nachverfolgung.|Nein|

## <a name="uri-scheme-semantics"></a>URI-Schemasemantik

Das `<ms-sway>` Schema definiert eine URI-Syntax zum Öffnen eines Sways oder zum Aufrufen der Sway-Anwendung. Das Schema definiert mehrere Befehlsargumente, die für folgende Aktionen verwendet werden können: 

- Öffnen Sie die Sway-Anwendung. &ndash; Es müssen keine Befehlsargumente angegeben werden. 

- Öffnen Sie ein Sway zur Anzeige in der Sway-Anwendung. Die für die Anzeige festgelegte ID und der &ndash; **Modus** müssen angegeben werden.  

- Öffnen Sie ein Sway zur Bearbeitung in der Sway-Anwendung. &ndash; Die **zu** bearbeitende ID und der zu bearbeitende **Modus** müssen angegeben werden. Es wird empfohlen, auch **den Authentifizierungs-Upn \_** und den **Authentifizierungs-PVR \_** einzuschließen, um sicherzustellen, dass beim Öffnen von Sway das richtige Konto mit Bearbeitungsberechtigungen verwendet wird.  

## <a name="example"></a>Beispiel

`ms-sway:id=CyrvEYLmFKi1B2_I&auth_upn=account@email.com&auth_pvr=WindowsLiveId&invoking_app=MyApp` 


