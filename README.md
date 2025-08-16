# Magnolia-Mobile-Golf
Mobile Golf Simulator Service
import React from "react"; import { Button } from "@/components/ui/button"; import { Card, CardContent, CardDescription, CardHeader, CardTitle } from "@/components/ui/card"; import { Input } from "@/components/ui/input"; import { Textarea } from "@/components/ui/textarea"; import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs"; import { Accordion, AccordionContent, AccordionItem, AccordionTrigger } from "@/components/ui/accordion"; import { Check, Phone, Mail, CalendarDays, MapPin, Star, Golf as GolfIcon, ArrowRight, Clock, ShieldCheck, Sparkles, Instagram, Facebook } from "lucide-react";

// ---------- // Helper Components // ---------- const Section = ({ id, className = "", children }: React.PropsWithChildren<{ id?: string; className?: string }>) => (

  <section id={id} className={`py-20 sm:py-24 ${className}`}>{children}</section>
);const Container = ({ children, className = "" }: React.PropsWithChildren<{ className?: string }>) => (

  <div className={`mx-auto w-full max-w-7xl px-5 sm:px-8 ${className}`}>{children}</div>
);const FeatureItem = ({ icon: Icon, title, desc }: { icon: any; title: string; desc: string }) => (

  <div className="flex items-start gap-4">
    <div className="rounded-2xl p-3 shadow-sm ring-1 ring-black/10"><Icon className="h-6 w-6" /></div>
    <div>
      <h4 className="font-semibold">{title}</h4>
      <p className="text-muted-foreground">{desc}</p>
    </div>
  </div>
);// ---------- // Main Page // ---------- export default function MobileGolfSimulator() { return ( <div className="min-h-screen bg-white text-slate-900"> {/* Header */} <header className="sticky top-0 z-50 w-full border-b bg-white/80 backdrop-blur supports-[backdrop-filter]:bg-white/60"> <Container className="flex h-16 items-center justify-between"> <a href="#" className="flex items-center gap-2"> <div className="flex h-9 w-9 items-center justify-center rounded-xl bg-emerald-600 text-white"><GolfIcon className="h-5 w-5" /></div> <span className="text-lg font-bold tracking-tight">OnPar Mobile Sims</span> </a> <nav className="hidden items-center gap-6 md:flex"> <a href="#services" className="text-sm font-medium hover:text-emerald-700">Services</a> <a href="#pricing" className="text-sm font-medium hover:text-emerald-700">Pricing</a> <a href="#gallery" className="text-sm font-medium hover:text-emerald-700">Gallery</a> <a href="#faq" className="text-sm font-medium hover:text-emerald-700">FAQ</a> <a href="#contact" className="text-sm font-medium hover:text-emerald-700">Contact</a> </nav> <div className="hidden md:block"> <a href="#booking"><Button className="rounded-2xl">Book Now</Button></a> </div> </Container> </header>

{/* Hero */}
  <Section>
    <Container className="grid items-center gap-10 lg:grid-cols-2">
      <div>
        <span className="inline-flex items-center gap-2 rounded-full border px-3 py-1 text-xs font-medium text-muted-foreground">
          <Sparkles className="h-3.5 w-3.5" /> New: Summer tournament packages
        </span>
        <h1 className="mt-4 text-4xl font-extrabold tracking-tight sm:text-5xl">
          Bring the Course to You —
          <span className="block text-emerald-600">Anytime. Anywhere.</span>
        </h1>
        <p className="mt-4 text-lg text-muted-foreground">
          We deliver a premium, climate‑controlled golf simulator to your driveway, office, or event. Rain or shine, day or night — perfect for parties, team building, or serious practice.
        </p>
        <div className="mt-6 flex flex-wrap items-center gap-3">
          <a href="#booking"><Button size="lg" className="rounded-2xl">Reserve a Date <ArrowRight className="ml-2 h-4 w-4" /></Button></a>
          <a href="#pricing"><Button size="lg" variant="outline" className="rounded-2xl">See Pricing</Button></a>
        </div>
        <div className="mt-6 flex flex-wrap items-center gap-6 text-sm text-muted-foreground">
          <div className="flex items-center gap-2"><ShieldCheck className="h-4 w-4" /> Fully Insured</div>
          <div className="flex items-center gap-2"><Clock className="h-4 w-4" /> Setup in ~30 minutes</div>
          <div className="flex items-center gap-2"><Star className="h-4 w-4" /> 5★ local service</div>
        </div>
      </div>
      <div>
        <div className="relative aspect-[4/3] w-full overflow-hidden rounded-3xl shadow-xl ring-1 ring-black/10">
          {/* Placeholder hero image */}
          <img src="https://images.unsplash.com/photo-1512422118476-89c974a3182e?q=80&w=1600&auto=format&fit=crop" alt="Mobile golf simulator trailer set up at a backyard event" className="h-full w-full object-cover" />
          <div className="pointer-events-none absolute inset-0 bg-gradient-to-tr from-black/10 via-transparent to-transparent" />
        </div>
      </div>
    </Container>
  </Section>

  {/* Services */}
  <Section id="services" className="bg-slate-50">
    <Container>
      <div className="mx-auto mb-12 max-w-2xl text-center">
        <h2 className="text-3xl font-bold tracking-tight sm:text-4xl">What We Bring</h2>
        <p className="mt-3 text-muted-foreground">Tour‑level tech in a compact, mobile setup. We handle delivery, setup, and coaching so you can swing away.</p>
      </div>
      <div className="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
        <Card className="rounded-2xl">
          <CardHeader>
            <CardTitle>Premium Simulator</CardTitle>
            <CardDescription>High‑speed camera/launch monitor, 4K projector, pro hitting mat, and safety enclosure.</CardDescription>
          </CardHeader>
          <CardContent className="space-y-4">
            <FeatureItem icon={Check} title="Top courses" desc="Play Pebble, St Andrews & more*" />
            <FeatureItem icon={Check} title="Ball & club data" desc="Carry, spin, speed, path, face, and more" />
            <FeatureItem icon={Check} title="Weather‑proof" desc="Climate controlled for year‑round comfort" />
            <p className="text-xs text-muted-foreground">*Course library varies by package.</p>
          </CardContent>
        </Card>
        <Card className="rounded-2xl">
          <CardHeader>
            <CardTitle>Event‑Ready Setup</CardTitle>
            <CardDescription>Ideal for birthdays, corporate events, fundraisers, or league nights.</CardDescription>
          </CardHeader>
          <CardContent className="space-y-4">
            <FeatureItem icon={Check} title="Tournament modes" desc="Closest‑to‑pin, long drive, and team scrambles" />
            <FeatureItem icon={Check} title="Branding" desc="Custom on‑screen logos & signage available" />
            <FeatureItem icon={Check} title="Attendant included" desc="We run the tech so you can enjoy the event" />
          </CardContent>
        </Card>
        <Card className="rounded-2xl">
          <CardHeader>
            <CardTitle>Coaching & Practice</CardTitle>
            <CardDescription>Dial in your swing with instant feedback and optional coaching add‑ons.</CardDescription>
          </CardHeader>
          <CardContent className="space-y-4">
            <FeatureItem icon={Check} title="Gapping sessions" desc="Know your carries across the bag" />
            <FeatureItem icon={Check} title="Video review" desc="Side‑by‑side swing analysis on‑site" />
            <FeatureItem icon={Check} title="Junior friendly" desc="Light clubs & fun games for kids" />
          </CardContent>
        </Card>
      </div>
    </Container>
  </Section>

  {/* Pricing */}
  <Section id="pricing">
    <Container>
      <div className="mx-auto mb-12 max-w-2xl text-center">
        <h2 className="text-3xl font-bold tracking-tight sm:text-4xl">Simple, Transparent Pricing</h2>
        <p className="mt-3 text-muted-foreground">Travel within 25 miles included. All packages include delivery, setup, and an on‑site attendant.</p>
      </div>
      <div className="grid gap-6 lg:grid-cols-3">
        <Card className="rounded-2xl border-2 border-emerald-600">
          <CardHeader>
            <CardTitle>Weeknight</CardTitle>
            <CardDescription>Mon–Thu, start after 4pm</CardDescription>
          </CardHeader>
          <CardContent className="space-y-4">
            <div className="text-4xl font-extrabold">$349<span className="text-lg font-medium text-muted-foreground"> / 2 hrs</span></div>
            <ul className="space-y-2 text-sm text-muted-foreground">
              <li>• Addl. hour: $125</li>
              <li>• Up to 12 golfers</li>
              <li>• Tournament games included</li>
            </ul>
            <a href="#booking"><Button className="mt-2 w-full rounded-2xl">Book Weeknight</Button></a>
          </CardContent>
        </Card>
        <Card className="rounded-2xl">
          <CardHeader>
            <CardTitle>Weekend</CardTitle>
            <CardDescription>Fri–Sun, all day</CardDescription>
          </CardHeader>
          <CardContent className="space-y-4">
            <div className="text-4xl font-extrabold">$499<span className="text-lg font-medium text-muted-foreground"> / 3 hrs</span></div>
            <ul className="space-y-2 text-sm text-muted-foreground">
              <li>• Addl. hour: $150</li>
              <li>• Up to 16 golfers</li>
              <li>• Premium course pack</li>
            </ul>
            <a href="#booking"><Button variant="outline" className="mt-2 w-full rounded-2xl">Book Weekend</Button></a>
          </CardContent>
        </Card>
        <Card className="rounded-2xl">
          <CardHeader>
            <CardTitle>Corporate / Full‑Day</CardTitle>
            <CardDescription>Custom events & festivals</CardDescription>
          </CardHeader>
          <CardContent className="space-y-4">
            <div className="text-4xl font-extrabold">From $1,200<span className="text-lg font-medium text-muted-foreground"> / day</span></div>
            <ul className="space-y-2 text-sm text-muted-foreground">
              <li>• Branding & giveaways</li>
              <li>• Lead capture kiosk</li>
              <li>• Emcee / competitions</li>
            </ul>
            <a href="#contact"><Button variant="outline" className="mt-2 w-full rounded-2xl">Get a Quote</Button></a>
          </CardContent>
        </Card>
      </div>
      <p className="mt-6 text-center text-xs text-muted-foreground">Prices are example placeholders — update to your market.</p>
    </Container>
  </Section>

  {/* Gallery */}
  <Section id="gallery" className="bg-slate-50">
    <Container>
      <div className="mx-auto mb-10 max-w-2xl text-center">
        <h2 className="text-3xl font-bold tracking-tight sm:text-4xl">Gallery</h2>
        <p className="mt-3 text-muted-foreground">A few setups from recent events and private sessions.</p>
      </div>
      <div className="grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
        {["https://images.unsplash.com/photo-1548199973-03cce0bbc87b?q=80&w=1600&auto=format&fit=crop","https://images.unsplash.com/photo-1477764250597-dffe9f601ae8?q=80&w=1600&auto=format&fit=crop","https://images.unsplash.com/photo-1519681393784-d120267933ba?q=80&w=1600&auto=format&fit=crop","https://images.unsplash.com/photo-1502877338535-766e1452684a?q=80&w=1600&auto=format&fit=crop","https://images.unsplash.com/photo-1513415564515-763d91423bdd?q=80&w=1600&auto=format&fit=crop","https://images.unsplash.com/photo-1470229722913-7c0e2dbbafd3?q=80&w=1600&auto=format&fit=crop"].map((src, i) => (
          <div key={i} className="group relative aspect-video overflow-hidden rounded-2xl ring-1 ring-black/10">
            <img src={src} alt={`Mobile simulator event ${i + 1}`} className="h-full w-full object-cover transition-transform duration-500 group-hover:scale-105" />
          </div>
        ))}
      </div>
    </Container>
  </Section>

  {/* Booking */}
  <Section id="booking">
    <Container>
      <div className="grid gap-8 lg:grid-cols-2">
        <div>
          <h2 className="text-3xl font-bold tracking-tight sm:text-4xl">Ready to Play?</h2>
          <p className="mt-3 text-muted-foreground">Tell us about your event and preferred date. We’ll confirm availability and send next steps.</p>

          <Tabs defaultValue="event" className="mt-6">
            <TabsList className="rounded-2xl">
              <TabsTrigger value="event">Event Booking</TabsTrigger>
              <TabsTrigger value="practice">Practice Session</TabsTrigger>
            </TabsList>
            <TabsContent value="event" className="mt-4">
              <form onSubmit={(e) => e.preventDefault()} className="grid gap-4 rounded-3xl border p-4 sm:p-6">
                <div className="grid gap-4 sm:grid-cols-2">
                  <Input placeholder="Your name*" required className="rounded-xl" />
                  <Input type="email" placeholder="Email*" required className="rounded-xl" />
                  <Input type="tel" placeholder="Phone" className="rounded-xl" />
                  <Input type="text" placeholder="Event address / city" className="rounded-xl" />
                  <Input type="date" placeholder="Preferred date" className="rounded-xl" />
                  <Input type="time" placeholder="Start time" className="rounded-xl" />
                </div>
                <Textarea placeholder="Tell us about your event (guest count, occasion, parking/space details)" className="min-h-28 rounded-xl" />
                <Button type="submit" className="rounded-2xl">Request Availability</Button>
                <p className="text-xs text-muted-foreground">This demo form does not send data. Hook it up to your email or CRM.</p>
              </form>
            </TabsContent>
            <TabsContent value="practice" className="mt-4">
              <form onSubmit={(e) => e.preventDefault()} className="grid gap-4 rounded-3xl border p-4 sm:p-6">
                <div className="grid gap-4 sm:grid-cols-2">
                  <Input placeholder="Your name*" required className="rounded-xl" />
                  <Input type="email" placeholder="Email*" required className="rounded-xl" />
                  <Input type="tel" placeholder="Phone" className="rounded-xl" />
                  <Input type="date" placeholder="Preferred date" className="rounded-xl" />
                </div>
                <Textarea placeholder="Goals (gapping, lessons, league play)" className="min-h-28 rounded-xl" />
                <Button type="submit" className="rounded-2xl">Request Session</Button>
                <p className="text-xs text-muted-foreground">This demo form does not send data. Hook it up to your email or CRM.</p>
              </form>
            </TabsContent>
          </Tabs>
        </div>

        <div className="space-y-6">
          <div className="rounded-3xl bg-gradient-to-br from-emerald-600 to-emerald-500 p-6 text-white shadow-lg">
            <h3 className="text-2xl font-bold">How it works</h3>
            <ol className="mt-4 list-decimal space-y-2 pl-4 text-emerald-50">
              <li>We confirm your date and send an invoice & agreement.</li>
              <li>Arrive 45 min early to set up the simulator pod.</li>
              <li>Run your event & pack up — zero cleanup required.</li>
            </ol>
            <p className="mt-4 text-sm text-emerald-50">Requires a fairly level surface and standard power (20A). Footprint: ~20' x 10' x 10'.</p>
          </div>

          <Card className="rounded-2xl">
            <CardHeader>
              <CardTitle>Coverage Area</CardTitle>
              <CardDescription>Travel within 25 miles of downtown is included. Small fee beyond that.</CardDescription>
            </CardHeader>
            <CardContent className="flex items-center gap-3 text-sm text-muted-foreground">
              <MapPin className="h-4 w-4" /> Your City, ST — customize this.
            </CardContent>
          </Card>

          <Card className="rounded-2xl">
            <CardHeader className="pb-2">
              <CardTitle>Contact</CardTitle>
              <CardDescription>Reach out directly — we respond quickly.</CardDescription>
            </CardHeader>
            <CardContent className="space-y-2 text-sm text-muted-foreground">
              <div className="flex items-center gap-2"><Phone className="h-4 w-4" /><a href="tel:+15551234567" className="hover:underline">(555) 123‑4567</a></div>
              <div className="flex items-center gap-2"><Mail className="h-4 w-4" /><a href="mailto:hello@onparmobilesims.com" className="hover:underline">hello@onparmobilesims.com</a></div>
              <div className="flex items-center gap-2"><CalendarDays className="h-4 w-4" />Lead time: 1–2 weeks recommended</div>
            </CardContent>
          </Card>
        </div>
      </div>
    </Container>
  </Section>

  {/* Testimonials */}
  <Section className="bg-slate-50">
    <Container>
      <div className="mx-auto mb-10 max-w-2xl text-center">
        <h2 className="text-3xl font-bold tracking-tight sm:text-4xl">Loved by Golfers & Hosts</h2>
        <p className="mt-3 text-muted-foreground">Here’s what guests say after a round in our mobile bay.</p>
      </div>
      <div className="grid gap-6 md:grid-cols-3">
        {[{
          quote: "An absolute hit at our company picnic. The long‑drive contest got everyone cheering!",
          name: "Maya R.",
        }, {
          quote: "Incredible data and setup. I finally know my 7‑iron carry.",
          name: "Alex T.",
        }, {
          quote: "Birthday party MVP. Kids and adults took turns all night.",
          name: "Jordan P.",
        }].map((t, i) => (
          <Card className="rounded-2xl" key={i}>
            <CardContent className="flex h-full flex-col justify-between p-6">
              <p className="text-sm leading-relaxed">“{t.quote}”</p>
              <div className="mt-4 flex items-center gap-2 text-sm text-muted-foreground">
                <Star className="h-4 w-4 fill-current" />
                <Star className="h-4 w-4 fill-current" />
                <Star className="h-4 w-4 fill-current" />
                <Star className="h-4 w-4 fill-current" />
                <Star className="h-4 w-4 fill-current" />
                <span className="ml-2">{t.name}</span>
              </div>
            </CardContent>
          </Card>
        ))}
      </div>
    </Container>
  </Section>

  {/* FAQ */}
  <Section id="faq">
    <Container>
      <div className="mx-auto mb-10 max-w-2xl text-center">
        <h2 className="text-3xl font-bold tracking-tight sm:text-4xl">Frequently Asked Questions</h2>
        <p className="mt-3 text-muted-foreground">Don’t see your question? Send us a note — we’ll help out.</p>
      </div>
      <Accordion type="single" collapsible className="mx-auto max-w-3xl">
        <AccordionItem value="space">
          <AccordionTrigger>How much space do I need?</AccordionTrigger>
          <AccordionContent>
            Plan for roughly 20 feet long by 10 feet wide by 10 feet high. A level driveway or indoor venue works best.
          </AccordionContent>
        </AccordionItem>
        <AccordionItem value="power">
          <AccordionTrigger>What power is required?</AccordionTrigger>
          <AccordionContent>
            A standard 20A household circuit is sufficient. We bring extension cords and manage cable safety.
          </AccordionContent>
        </AccordionItem>
        <AccordionItem value="weather">
          <AccordionTrigger>What about rain or heat?</AccordionTrigger>
          <AccordionContent>
            Our bay is covered and climate‑controlled. We can operate in light rain and hot/cold conditions.
          </AccordionContent>
        </AccordionItem>
        <AccordionItem value="cancellation">
          <AccordionTrigger>What’s your cancellation policy?</AccordionTrigger>
          <AccordionContent>
            Full refund up to 7 days before the event. Within 7 days, we’ll reschedule at no cost subject to availability.
          </AccordionContent>
        </AccordionItem>
      </Accordion>
    </Container>
  </Section>

  {/* Contact */}
  <Section id="contact" className="bg-slate-50">
    <Container className="grid gap-8 lg:grid-cols-2">
      <div>
        <h2 className="text-3xl font-bold tracking-tight sm:text-4xl">Get in Touch</h2>
        <p className="mt-3 text-muted-foreground">Have a special request or large event? We’d love to hear the details.</p>
        <form onSubmit={(e) => e.preventDefault()} className="mt-6 grid gap-4 rounded-3xl border bg-white p-4 sm:p-6">
          <div className="grid gap-4 sm:grid-cols-2">
            <Input placeholder="Name*" required className="rounded-xl" />
            <Input type="email" placeholder="Email*" required className="rounded-xl" />
          </div>
          <Input type="tel" placeholder="Phone" className="rounded-xl" />
          <Textarea placeholder="Your message" className="min-h-28 rounded-xl" />
          <Button type="submit" className="rounded-2xl">Send Message</Button>
          <p className="text-xs text-muted-foreground">Demo only — connect to your email service to receive messages.</p>
        </form>
      </div>
      <div className="space-y-4">
        <Card className="rounded-2xl">
          <CardHeader>
            <CardTitle>Business Details</CardTitle>
            <CardDescription>Customize with your real info.</CardDescription>
          </CardHeader>
          <CardContent className="space-y-2 text-sm text-muted-foreground">
            <div className="flex items-center gap-2"><MapPin className="h-4 w-4" /> Based in Your City, ST</div>
            <div className="flex items-center gap-2"><Phone className="h-4 w-4" /><a href="tel:+15551234567" className="hover:underline">(555) 123‑4567</a></div>
            <div className="flex items-center gap-2"><Mail className="h-4 w-4" /><a className="hover:underline" href="mailto:hello@onparmobilesims.com">hello@onparmobilesims.com</a></div>
            <div className="flex items-center gap-2"><Instagram className="h-4 w-4" /> @onparmobilesims</div>
            <div className="flex items-center gap-2"><Facebook className="h-4 w-4" /> /onparmobilesims</div>
          </CardContent>
        </Card>

        <div className="rounded-3xl bg-gradient-to-r from-slate-900 to-slate-700 p-6 text-white">
          <h3 className="text-xl font-bold">Special Offer</h3>
          <p className="mt-1 text-sm text-slate-200">Weeknight bookings get a free closest‑to‑pin competition kit.</p>
          <a href="#booking"><Button variant="secondary" className="mt-3 rounded-2xl">Claim Offer</Button></a>
        </div>
      </div>
    </Container>
  </Section>

  {/* Footer */}
  <footer className="border-t">
    <Container className="flex flex-col items-center justify-between gap-4 py-8 sm:flex-row">
      <p className="text-sm text-muted-foreground">© {new Date().getFullYear()} OnPar Mobile Sims. All rights reserved.</p>
      <div className="flex items-center gap-6 text-sm">
        <a href="#services" className="hover:text-emerald-700">Services</a>
        <a href="#pricing" className="hover:text-emerald-700">Pricing</a>
        <a href="#booking" className="hover:text-emerald-700">Book</a>
        <a href="#contact" className="hover:text-emerald-700">Contact</a>
      </div>
    </Container>
  </footer>
</div>

); }

