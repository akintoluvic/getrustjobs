<script setup lang="ts">
import { Edit, PlusCircle, Upload } from 'lucide-vue-next';

</script>
<template>
  <GeneralSectionWrapper
    title="Manage your profile"
    description="Update your your profile to get jobs from around the globe."
    background-color="bg-white"
  >
  <main class="mt-12 grid flex-1 items-start gap-4 p-4 sm:px-6 sm:py-0 md:gap-8">
        <div class="mx-auto grid max-w-[59rem] flex-1 auto-rows-max gap-4">
          <div class="flex items-center gap-4">
            <span variant="outline" size="icon" class="h-7 w-7 grid place-items-center rounded border">
              <Edit class="h-4 w-4" />
              <span class="sr-only">Edit</span>
            </span>
            <h1 class="flex-1 shrink-0 whitespace-nowrap text-xl font-semibold tracking-tight sm:grow-0">
              Edit Profile
            </h1>
            
            <div class="hidden items-center gap-2 md:ml-auto md:flex">
              <Button variant="outline" size="sm">
                Discard
              </Button>
              <Button size="sm">
                Save Profile
              </Button>
            </div>
          </div>
          <div class="grid gap-4 md:grid-cols-[1fr_250px] lg:grid-cols-3 lg:gap-8">
            <div class="grid auto-rows-max items-start gap-4 lg:col-span-2 lg:gap-8">
              <Card>
                <CardHeader>
                  <CardTitle>Profile Details</CardTitle>
                  <CardDescription>
                    Lipsum dolor sit amet, consectetur adipiscing elit
                  </CardDescription>
                </CardHeader>
                <CardContent>
                  <div class="grid gap-6">
                    <div class="grid gap-3">
                      <Label for="name">Name</Label>
                      <Input
                        id="name"
                        type="text"
                        class="w-full"
                        default-value="Gamer Gear Pro Controller"
                      />
                    </div>
                    <div class="grid gap-3">
                      <Label for="description">Description</Label>
                      <Textarea
                        id="description"
                        default-value="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam auctor, nisl nec ultricies ultricies, nunc nisl ultricies nunc, nec ultricies nunc nisl nec nunc."
                        class="min-h-32"
                      />
                    </div>
                  </div>
                </CardContent>
              </Card>
              <Card>
                <CardHeader>
                  <CardTitle>Tech Stack</CardTitle>
                  <CardDescription>
                    Lipsum dolor sit amet, consectetur adipiscing elit
                  </CardDescription>
                </CardHeader>
                <CardContent>
                  <Table>
                    <TableHeader>
                      <TableRow>
                        <TableHead class="w-[100px]">
                          Tech
                        </TableHead>
                        <TableHead>Years of experience</TableHead>
                        <TableHead class="w-[100px]">
                          Proficiency
                        </TableHead>
                      </TableRow>
                    </TableHeader>
                    <TableBody>
                      <TableRow>
                        <TableCell class="font-semibold">
                          Rust
                        </TableCell>
                        <TableCell>
                          <Label for="stock-1" class="sr-only">
                            Stock
                          </Label>
                          <Input
                            id="stock-1"
                            type="number"
                            default-value="100"
                          />
                        </TableCell>
                        <TableCell>
                          <ToggleGroup
                            type="single"
                            default-value="s"
                            variant="outline"
                          >
                            <ToggleGroupItem value="s">
                              S
                            </ToggleGroupItem>
                            <ToggleGroupItem value="m">
                              M
                            </ToggleGroupItem>
                            <ToggleGroupItem value="l">
                              L
                            </ToggleGroupItem>
                          </ToggleGroup>
                        </TableCell>
                      </TableRow>
                      <TableRow>
                        <TableCell class="font-semibold">
                          PHP
                        </TableCell>
                        <TableCell>
                          <Label for="stock-2" class="sr-only">
                            Stock
                          </Label>
                          <Input
                            id="stock-2"
                            type="number"
                            default-value="143"
                          />
                        </TableCell>
                        <TableCell>
                          <ToggleGroup
                            type="single"
                            default-value="m"
                            variant="outline"
                          >
                            <ToggleGroupItem value="s">
                              S
                            </ToggleGroupItem>
                            <ToggleGroupItem value="m">
                              M
                            </ToggleGroupItem>
                            <ToggleGroupItem value="l">
                              L
                            </ToggleGroupItem>
                          </ToggleGroup>
                        </TableCell>
                      </TableRow>
                      <TableRow>
                        <TableCell class="font-semibold">
                          Javascript
                        </TableCell>
                        <TableCell>
                          <Label for="stock-3" class="sr-only">
                            Stock
                          </Label>
                          <Input
                            id="stock-3"
                            type="number"
                            default-value="32"
                          />
                        </TableCell>
                        <TableCell>
                          <ToggleGroup
                            type="single"
                            default-value="s"
                            variant="outline"
                          >
                            <ToggleGroupItem value="s">
                              S
                            </ToggleGroupItem>
                            <ToggleGroupItem value="m">
                              M
                            </ToggleGroupItem>
                            <ToggleGroupItem value="l">
                              L
                            </ToggleGroupItem>
                          </ToggleGroup>
                        </TableCell>
                      </TableRow>
                    </TableBody>
                  </Table>
                </CardContent>
                <CardFooter class="justify-center border-t p-4">
                  <Button size="sm" variant="ghost" class="gap-1">
                    <PlusCircle class="h-3.5 w-3.5" />
                    Add Variant
                  </Button>
                </CardFooter>
              </Card>
              <Card>
                <CardHeader>
                  <CardTitle>Profile Category</CardTitle>
                </CardHeader>
                <CardContent>
                  <div class="grid gap-6 sm:grid-cols-3">
                    <div class="grid gap-3">
                      <Label for="category">Category</Label>
                      <Select>
                        <SelectTrigger
                          id="category"
                          aria-label="Select category"
                        >
                          <SelectValue placeholder="Select category" />
                        </SelectTrigger>
                        <SelectContent>
                          <SelectItem value="clothing">
                            Clothing
                          </SelectItem>
                          <SelectItem value="electronics">
                            Electronics
                          </SelectItem>
                          <SelectItem value="accessories">
                            Accessories
                          </SelectItem>
                        </SelectContent>
                      </Select>
                    </div>
                    <div class="grid gap-3">
                      <Label for="subcategory">
                        Subcategory (optional)
                      </Label>
                      <Select>
                        <SelectTrigger
                          id="subcategory"
                          aria-label="Select subcategory"
                        >
                          <SelectValue placeholder="Select subcategory" />
                        </SelectTrigger>
                        <SelectContent>
                          <SelectItem value="t-shirts">
                            T-Shirts
                          </SelectItem>
                          <SelectItem value="hoodies">
                            Hoodies
                          </SelectItem>
                          <SelectItem value="sweatshirts">
                            Sweatshirts
                          </SelectItem>
                        </SelectContent>
                      </Select>
                    </div>
                  </div>
                </CardContent>
              </Card>
            </div>
            <div class="grid auto-rows-max items-start gap-4 lg:gap-8">
              <Card>
                <CardHeader>
                  <CardTitle>Profile Status</CardTitle>
                </CardHeader>
                <CardContent>
                  <div class="grid gap-6">
                    <div class="grid gap-3">
                      <Label for="status">Status</Label>
                      <Select>
                        <SelectTrigger id="status" aria-label="Select status">
                          <SelectValue placeholder="Select status" />
                        </SelectTrigger>
                        <SelectContent>
                          <SelectItem value="draft">
                            Draft
                          </SelectItem>
                          <SelectItem value="published">
                            Active
                          </SelectItem>
                          <SelectItem value="archived">
                            Archived
                          </SelectItem>
                        </SelectContent>
                      </Select>
                    </div>
                  </div>
                </CardContent>
              </Card>
              <Card class="overflow-hidden">
                <CardHeader>
                  <CardTitle>Profile Picture</CardTitle>
                  <CardDescription>
                    Lipsum dolor sit amet, consectetur adipiscing elit
                  </CardDescription>
                </CardHeader>
                <CardContent>
                  <div class="grid gap-2">
                    <img
                      alt="Profile image"
                      class="aspect-square w-full rounded-md object-cover"
                      height="300"
                      src="https://images.unsplash.com/photo-1598257006458-087169a1f08d?q=80&w=2970&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                      width="300"
                    >
                    <Button class="flex gap-2 w-full items-center justify-center rounded-md">
                      <Upload class="h-4 w-4 text-white" />
                      <span class="sr-onl">Upload Profile Picture</span>
                    </Button>
                  </div>
                </CardContent>
              </Card>
              <Card>
                <CardHeader>
                  <CardTitle>Archive Profile</CardTitle>
                  <CardDescription>
                    Lipsum dolor sit amet, consectetur adipiscing elit.
                  </CardDescription>
                </CardHeader>
                <CardContent>
                  <div />
                  <Button size="sm" variant="secondary">
                    Archive Profile
                  </Button>
                </CardContent>
              </Card>
            </div>
          </div>
          <div class="flex items-center justify-center gap-2 md:hidden">
            <Button variant="outline" size="sm">
              Discard
            </Button>
            <Button size="sm">
              Save Profile
            </Button>
          </div>
        </div>
      </main>
  </GeneralSectionWrapper>
  
</template>