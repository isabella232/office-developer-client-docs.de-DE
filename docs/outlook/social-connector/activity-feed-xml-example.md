---
title: Beispiel für eine Aktivität Feed XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: Das XML-Beispiel in diesem Thema wird, dass ein Aktivitätsfeed an Outlook Social Connector (OSC) zurückgegeben, nachdem sie die ISocialSession2::GetActivitiesEx-Methode für ein social Network ruft XML-Zeichenfolge.
ms.openlocfilehash: ab27ddfad5044994a19bb32759994a0e98c39ae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795947"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="156fe-103">Beispiel für eine Aktivität Feed XML</span><span class="sxs-lookup"><span data-stu-id="156fe-103">Activity Feed XML Example</span></span>

<span data-ttu-id="156fe-104">Das XML-Beispiel in diesem Thema wird ein Aktivitätsfeed an Outlook Social Connector (OSC) zurückgegeben, nachdem sie die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode für ein social Network ruft XML-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="156fe-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="156fe-105">Das Beispiel zeigt die **ActivityFeed** XML, das die folgenden vier Aktivitäten enthält, jeweils getrennt durch das Element **ActivityDetails** und matching eine Vorlage für die Zwecke anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="156fe-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="156fe-106">Ein Profilbild aktualisieren, indem Sie Melissa Macbeth, dessen **OwnerID** im sozialen Netzwerk 4667647 ist.</span><span class="sxs-lookup"><span data-stu-id="156fe-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="156fe-107">Diese Aktivität gibt drei Vorlagenvariablen vom Typ **PublisherVariable**, **ListVariable**und **PictureVariable** (die in **ListVariable**eingeschlossen wird).</span><span class="sxs-lookup"><span data-stu-id="156fe-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="156fe-108">Diese Variablen geben die Person, die die Aktivitätsfeed Element und Informationen für das Bild zu aktualisierenden (mithilfe der **Name**, **Value**, **AltText**und **Href** untergeordnete Elemente des **PictureVariable**) veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="156fe-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="156fe-109">Ein Profilbild aktualisieren, indem Sie Michael Affronti, deren **OwnerID** im sozialen Netzwerk 5015012 ist.</span><span class="sxs-lookup"><span data-stu-id="156fe-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="156fe-110">Ähnlich wie die letzte Aktivität, gibt diese Aktivität drei Vorlagenvariablen vom Typ **PublisherVariable**, **ListVariable**und **PictureVariable**.</span><span class="sxs-lookup"><span data-stu-id="156fe-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="156fe-111">Diese Variablen geben die Person, die die Aktivitätsfeed Element und Informationen für das Bild zu aktualisierenden veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="156fe-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="156fe-112">Von Michael Affronti, mit der gleichen **OwnerID** des 5015012 als die letzte Aktivität Statusinformationen.</span><span class="sxs-lookup"><span data-stu-id="156fe-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="156fe-113">Diese Aktivität gibt zwei Vorlagenvariablen vom Typ **PublisherVariable** und **TextVariable**an.</span><span class="sxs-lookup"><span data-stu-id="156fe-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="156fe-114">**PublisherVariable** gibt die Person, die die Aktivitätsfeed Element veröffentlicht und **TextVariable** enthält den **Wert** der Statuszeile`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="156fe-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="156fe-115">Von Michael Affronti, mit der gleichen **OwnerID** des 5015012 als die letzten beiden Aktivitäten Blogbeitrag.</span><span class="sxs-lookup"><span data-stu-id="156fe-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="156fe-116">Diese Aktivität gibt zwei Vorlagenvariablen vom Typ **PublisherVariable** und **LinkVariable**an.</span><span class="sxs-lookup"><span data-stu-id="156fe-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="156fe-117">**PublisherVariable** gibt die Person, die die Aktivität veröffentlicht feed Element und **LinkVariable** enthält weitere Informationen (angegeben durch den **Namen**, **Text**und **Value** untergeordnete Elemente des **LinkVariable**) Informationen zu den Blogbeitrag.</span><span class="sxs-lookup"><span data-stu-id="156fe-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="156fe-118">Jede der vier Aktivitäten gibt einen **TemplateID** -Wert, der eine der drei Vorlagen für die **Vorlagen** -Element angegebenen entspricht.</span><span class="sxs-lookup"><span data-stu-id="156fe-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="156fe-119">Jede Vorlage ist in einem eigenen **ActivityTemplateContainer** -Element identifizierten ein **TemplateID** -Wert, der auch verwendet wird, um eine Aktivität anzuzeigen, die den gleichen Wert **TemplateID** verfügt.</span><span class="sxs-lookup"><span data-stu-id="156fe-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="156fe-120">Eine ausführliche Beschreibung der XML-Elemente im Beispiel verwendet finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="156fe-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="156fe-121">Übersicht über XML-Code für eine Aktivität Element-Feed</span><span class="sxs-lookup"><span data-stu-id="156fe-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="156fe-122">ActivityDetails Element</span><span class="sxs-lookup"><span data-stu-id="156fe-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="156fe-123">ActivityTemplateContainer Element</span><span class="sxs-lookup"><span data-stu-id="156fe-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="156fe-124">Vorlagenvariablen</span><span class="sxs-lookup"><span data-stu-id="156fe-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="156fe-125">XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="156fe-125">XML example</span></span>

<span data-ttu-id="156fe-126">Das folgende Beispiel zeigt die XML-Daten des vier Aktivitäten **ActivityFeed** : zwei Bild Updates, Statusinformationen und Blogbeiträgen profile.</span><span class="sxs-lookup"><span data-stu-id="156fe-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="156fe-127">Der XML-Code gibt zudem drei Aktivität Anzeigevorlagen für den zugehörigen Aktivitäten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="156fe-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <network>Contoso</network>
  <activities>
    <activityDetails>
      <ownerID>4667647</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a31</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-05T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>4667647</id>
          <nameHint>Melissa Macbeth</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a32</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-08T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a38</objectID>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <publishDate>2010-03-08T18:30:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com</profileUrl>
        </templateVariable>
        <templateVariable type="textVariable">
          <name>statusText</name>
          <value>is hiking on Mount Rainier this weekend!</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a39</objectID>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <publishDate>2010-03-04T15:00:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>http://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
  </activities>
  <templates>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <activityTemplate>
        <type>Photo</type>
        <title>{publisher:Publisher} has a new profile photo: </title>
        <data>{list:ProfilePhoto({picture:Photo})}</data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a><span data-ttu-id="156fe-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="156fe-128">See also</span></span>

- [<span data-ttu-id="156fe-129">OSC-Anbieter XML-Beispielen</span><span class="sxs-lookup"><span data-stu-id="156fe-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="156fe-130">XML-Code für Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="156fe-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="156fe-131">Funktionen XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="156fe-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="156fe-132">Freunde XML-Beispiel</span><span class="sxs-lookup"><span data-stu-id="156fe-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="156fe-133">Outlook Connector für soziale Netzwerke Anbieter XML-Schema</span><span class="sxs-lookup"><span data-stu-id="156fe-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

