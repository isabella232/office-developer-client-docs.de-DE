---
title: Testen die folgenden und Stop-folgenden Personen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c603c3c6-62c8-4895-93e1-b2e146dfaa4f
description: In diesem Thema werden die Szenarien zum Testen des Outlook Social Connector (OSC)-Anbieters Möglichkeit, führen einen Freund, und beenden Sie einen Freund auf dem sozialen Netzwerk folgen.
ms.openlocfilehash: 09652b658a2c20301b8b0568d373ae6fe841fe2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796078"
---
# <a name="testing-following-and-stop-following-persons"></a><span data-ttu-id="6daf9-103">Testen die folgenden und Stop-folgenden Personen</span><span class="sxs-lookup"><span data-stu-id="6daf9-103">Testing following and stop-following persons</span></span>

<span data-ttu-id="6daf9-104">In diesem Thema werden die Szenarien zum Testen des Outlook Social Connector (OSC)-Anbieters Möglichkeit, führen einen Freund, und beenden Sie einen Freund auf dem sozialen Netzwerk folgen.</span><span class="sxs-lookup"><span data-stu-id="6daf9-104">This topic describes scenarios to test the Outlook Social Connector (OSC) provider's ability to follow a friend, and to stop following a friend on the social network.</span></span>
  
## <a name="following-a-person"></a><span data-ttu-id="6daf9-105">Nach einer Person</span><span class="sxs-lookup"><span data-stu-id="6daf9-105">Following a person</span></span>

<span data-ttu-id="6daf9-106">Um eine Person folgen werden eine Person als Freund im sozialen Netzwerk, die SMTP-Adresse zur Verfügung gestellt, durch das ausgewählte Outlook-Element hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6daf9-106">To follow a person is to add a person as a friend on the social network, using the SMTP address provided by the selected Outlook item.</span></span> <span data-ttu-id="6daf9-107">Nach einer Person in der Regel in einem sozialen Netzwerk umfasst anfordern Berechtigung von dieser Person per e-Mail an diese SMTP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="6daf9-107">Following someone on a social network usually involves requesting permission from that person by an email to that SMTP address.</span></span> <span data-ttu-id="6daf9-108">Um die Berechtigung zu erteilen, die Person muss entweder haben, SMTP-Adresse, die bereits in seinem für soziale Netzwerkkonto enthalten oder bereit sind, hinzufügen, SMTP in ein Konto für soziale Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="6daf9-108">In order to grant permission, that person must either have that SMTP address already included in his or her social network account, or be willing to add that SMTP to a social network account.</span></span> <span data-ttu-id="6daf9-109">Testen Sie die folgenden Szenarien stellen Sie sicher, dass Ihre OSC-Anbieter richtig funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6daf9-109">Test each of the following scenarios to verify that your OSC provider behaves correctly.</span></span>
  
|<span data-ttu-id="6daf9-110">**Szenario**</span><span class="sxs-lookup"><span data-stu-id="6daf9-110">**Scenario**</span></span>|<span data-ttu-id="6daf9-111">**Erwartetes Verhalten**</span><span class="sxs-lookup"><span data-stu-id="6daf9-111">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6daf9-112">Beim Versuch, führen eine Person auf soziale Netzwerke, die im sozialen Netzwerk vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6daf9-112">Attempting to follow a person on the social network who exists on the social network.</span></span>  <br/> |<span data-ttu-id="6daf9-113">Für ein social Network, die keine Berechtigung, die von der Person erforderlich ist, fügt den Benutzer als Freund sofort für soziale Netzwerke hinzu.</span><span class="sxs-lookup"><span data-stu-id="6daf9-113">For a social network that does not require permission from the person, the social network immediately adds the person as a friend.</span></span>  <br/> <span data-ttu-id="6daf9-114">Für ein Netzwerk, die von dieser Person die Berechtigung benötigt, sendet das soziale Netzwerk eine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="6daf9-114">For a network that requires permission from that person, the social network sends a notification.</span></span> <span data-ttu-id="6daf9-115">Bereich Personen Outlook eine ausstehende Symbol für diese Person angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6daf9-115">The Outlook People Pane displays a pending icon for that person.</span></span>  <br/> |
|<span data-ttu-id="6daf9-116">Beim Versuch, führen eine Person auf soziale Netzwerke, die nicht im sozialen Netzwerk vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6daf9-116">Attempting to follow a person on the social network who does not exist on the social network.</span></span>  <br/> |<span data-ttu-id="6daf9-117">Der OSC-Anbieter den entsprechenden Fehler in [ISocialSession::FollowPerson](isocialsession-followperson.md) oder [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6daf9-117">The OSC provider displays the appropriate error in [ISocialSession::FollowPerson](isocialsession-followperson.md) or [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md).</span></span>  <br/> |
|<span data-ttu-id="6daf9-118">Auf dem sozialen Netzwerk einen Freund folgen.</span><span class="sxs-lookup"><span data-stu-id="6daf9-118">Following a friend on the social network.</span></span>  <br/> |<span data-ttu-id="6daf9-119">Für die Friend im Bereich Personen ausgewählt ist werden dem sozialen Netzwerk-Logo und die Friend Profil Teile des Bildes für das soziale Netzwerk angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6daf9-119">For the friend selected in the People Pane, the social network's badge and the friend's profile picture for that social network are displayed.</span></span>  <br/> |
|<span data-ttu-id="6daf9-120">Die Verknüpfung auf der Profilseite des einen Freund auswählen.</span><span class="sxs-lookup"><span data-stu-id="6daf9-120">Selecting the link to the profile page of a friend.</span></span>  <br/> |<span data-ttu-id="6daf9-121">Die Friend-Seite im sozialen Netzwerk im Standardbrowser des angemeldeten Benutzers wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6daf9-121">The friend's page on the social network opens in the logged-on user's default browser.</span></span>  <br/> |
   
## <a name="stop-following-a-person"></a><span data-ttu-id="6daf9-122">Beenden Sie nach einer person</span><span class="sxs-lookup"><span data-stu-id="6daf9-122">Stop following a person</span></span>

<span data-ttu-id="6daf9-123">Um nach einer Person zu beenden ist diese Person als Freund im sozialen Netzwerk zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6daf9-123">To stop following a person is to remove that person as a friend on the social network.</span></span> <span data-ttu-id="6daf9-124">Testen Sie das folgende Szenario, um Ihre OSC-Anbieter wird beendet, die nach einer Person ordnungsgemäß zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6daf9-124">Test the following scenario to verify your OSC provider stops following a person properly.</span></span>
  
|<span data-ttu-id="6daf9-125">**Szenario**</span><span class="sxs-lookup"><span data-stu-id="6daf9-125">**Scenario**</span></span>|<span data-ttu-id="6daf9-126">**Erwartetes Verhalten**</span><span class="sxs-lookup"><span data-stu-id="6daf9-126">**Expected behavior**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6daf9-127">Versucht, eine Person als Freund im sozialen Netzwerk zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="6daf9-127">Attempting to remove a person as a friend on the social network.</span></span>  <br/> |<span data-ttu-id="6daf9-128">Soziale Netzwerke werden nicht mehr die Person als Freund Konto des angemeldeten Benutzers aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6daf9-128">The social network no longer lists that person as a friend on the logged on user's account.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6daf9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6daf9-129">See also</span></span>

- [<span data-ttu-id="6daf9-130">Vorbereitung der Freigabe eines OSC-Providers</span><span class="sxs-lookup"><span data-stu-id="6daf9-130">Getting Ready to Release an OSC Provider</span></span>](getting-ready-to-release-an-osc-provider.md)

